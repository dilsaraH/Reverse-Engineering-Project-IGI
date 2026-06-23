# Reverse Engineering Project IGI
<p>This project demonstrates the reverse engineering and runtime patching of Project I.G.I. using Ghidra and x32dbg. The repository includes the modified game files, screenshots, and supporting resources used throughout the analysis.If you're interested in the technical details, a full report is available in the documentation folder covering the methodology, memory analysis, assembly modifications, and security discussion. Feel free to dive into the documentation if you're into that kind of stuff.</p>

<h3>Objectives</h3>
<ul>
  <li>Analyze the executable structure of Project I.G.I.</li>
  <li>Identify the ammunition handling logic.</li>
  <li>Trace memory and register activity during gameplay.</li>
  <li>Locate the instruction responsible for ammo reduction.</li>
  <li>Apply an assembly-level patch to modify program behavior.</li>
  <li>Evaluate the security weaknesses that allow runtime manipulation.</li>
</ul>  

<h3>Tools Used</h3>
<ul>
  <li>Ghidra</li>
  <li>x32dbg</li>
  <li>VMware Workstation</li>
  <li>Windows 10 Virtual Machine</li>
</ul>

<h3>Methodology</h3>

The project followed four major phases:<br/>
<ol>
  <li><b>Static Analysis</b></li>
    <ul>
      <li>Decompiled the executable using Ghidra.</li>
      <li>Identified functions related to weapon firing and ammunition handling.</li>
    </ul>
  <li><b>Dynamic Analysis</b></li>
    <ul>
      <li>Attached x32dbg to the running game process.</li>
      <li>Set breakpoints and monitored instruction execution.</li>
    </ul>
  <li><b>Memory Verification</b></li>
    <ul>
      <li>Tracked memory locations and CPU registers.</li>
      <li>Confirmed the relationship between the ammo value and the assembly instructions.</li>
    </ul>
  <li><b>Runtime Patching</b></li>
      <ul>
        <li>Replaced the DEC EAX instruction with NOP.</li>
        <li>Prevented ammunition values from decreasing during gameplay.</li>
      </ul>
</ol>
<h3>Repository Contents</h3>
<ul>
  <li>Modified game files</li>
  <li>Analysis documentation</li>
</ul>
<b>This repository was created for academic and cybersecurity research purposes to demonstrate reverse engineering methodologies, software analysis techniques, and the importance of secure software design.</b>
