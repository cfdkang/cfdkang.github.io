# Postdoctoral Researcher

Hi everyone! I am now a postdoctoral researcher in Mechanical and Aerospace Engineering at UC San Diego since October 2024. My current project is to enhance acoustic prediction capabilities of Comprehensive Analysis high-Dimensional Design Environment systems (CADDEE) based on Computational System Design Language (CSDL). This is supported by my PI, Prof. John T. Hwang. The research keywords are Multidisciplinary Design Optimization (MDO), aircraft design, and sensitivity analysis. I am also interested in computational fluid dynamics (CFD) and aeroacoustics.

# My Research Topics and Publications

<!-- Tab navigation -->
<div>
  <button onclick="openTab(event, 'Research')" id="defaultTab">Research Topics</button>
  <button onclick="openTab(event, 'Publications')">Publications</button>
</div>

<!-- Tab content -->
<div id="Research" class="tabcontent">
  ## Research Topics
  - **Topic 1**: Computational fluid dynamics and acoustics
  - **Topic 2**: Noise prediction and validation models
  - **Topic 3**: Optimization for aeroacoustics design
</div>

<div id="Publications" class="tabcontent">
  ## Publications
  1. Doe, J., & Smith, A. (2023). "Noise Modeling for Advanced Airfoils." *Journal of Aeroacoustics*.  
  2. Doe, J., & Smith, A. (2022). "Computational Efficiency in CFD." *Journal of Fluid Mechanics*.
  3. Doe, J., & Smith, A. (2021). "Optimization of Rotor Designs." *AIAA Journal*.
</div>

<!-- CSS for tabs -->
<style>
  .tabcontent { display: none; padding: 10px; border: 1px solid #ccc; }
  button { margin: 5px; padding: 10px; cursor: pointer; }
</style>

<!-- JavaScript for tabs -->
<script>
  function openTab(evt, tabName) {
    // Hide all tabcontent
    var i, tabcontent, buttons;
    tabcontent = document.getElementsByClassName('tabcontent');
    for (i = 0; i < tabcontent.length; i++) {
      tabcontent[i].style.display = 'none';
    }

    // Highlight the current tab and show its content
    buttons = document.getElementsByTagName('button');
    for (i = 0; i < buttons.length; i++) {
      buttons[i].style.backgroundColor = '';
    }
    document.getElementById(tabName).style.display = 'block';
    evt.currentTarget.style.backgroundColor = '#ddd';
  }

  // Open the default tab
  document.getElementById('defaultTab').click();
</script>
