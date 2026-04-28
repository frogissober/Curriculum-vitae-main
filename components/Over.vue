<template>
  <div id="over">
    <div class="ik">
      <div class="flex column">
        <span class="naam">floris</span> <span class="achternaam">Bogers</span>
      </div>
        <span class="adres">Nieuwe Heilaarstraat 37 - 4813AR  BREDA - +31 6 36493167 - <span class="email"><a href="mailto:floris@tonbogers.nl">floris@tonbogers.nl</a></span></span>
    </div>
    <div class="content">
      <p v-for="paragraph in $t('over.description').split('\n\n')" :key="paragraph">
        {{ paragraph }}
      </p>
    </div>
    <div class="socials">
      <a href="https://www.linkedin.com/in/floris-bogers-42ab26224/" target="_blank" class="linkedin">
        <div class="circle">
          <font-awesome-icon :icon="['fab', 'linkedin-in']" class="icon alt" style="font-size:30px" />
        </div>
      </a>
      <a href="https://github.com/ItzFloris" target="_blank" class="linkedin">
        <div class="circle">
          <font-awesome-icon :icon="['fab', 'github']" class="icon alt" style="font-size:30px" />
        </div>
      </a>
      <button @click="downloadPDF" class="download-link">
        <div class="circle">
          <font-awesome-icon :icon="['fas', 'download']" class="icon alt" style="font-size:30px" />
        </div>
      </button>
    </div>
    <hr>
  </div>
</template>

<script>
import html2canvas from 'html2canvas';
import jsPDF from 'jspdf';

export default {
  methods: {
    async downloadPDF() {
      try {
        const element = document.querySelector('#main');
        const locale = this.$i18n.locale;
        const filename = locale === 'nl' ? 'CV_Floris_Bogers.pdf' : 'CV_Floris_Bogers_EN.pdf';
        
        // Convert the HTML element to canvas
        const canvas = await html2canvas(element, {
          scale: 2,
          allowTaint: true,
          useCORS: true,
          backgroundColor: '#ffffff'
        });
        
        // Get canvas dimensions
        const imgWidth = 210; // A4 width in mm
        const pageHeight = 295; // A4 height in mm
        const imgHeight = (canvas.height * imgWidth) / canvas.width;
        
        // Create PDF
        const pdf = new jsPDF('p', 'mm', 'a4');
        let heightLeft = imgHeight;
        let position = 0;
        
        const imgData = canvas.toDataURL('image/png');
        
        // Add image to PDF, with multiple pages if needed
        while (heightLeft >= 0) {
          pdf.addImage(imgData, 'PNG', 0, position, imgWidth, imgHeight);
          heightLeft -= pageHeight;
          if (heightLeft > 0) {
            pdf.addPage();
            position = heightLeft - imgHeight;
          }
        }
        
        pdf.save(filename);
      } catch (error) {
        console.error('Error generating PDF:', error);
      }
    }
  }
}
</script>

