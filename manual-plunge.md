---
title: Manual-Plunging | Herzik Lab
layout: default
---
<div class="container">
 <div class="row">
   <div class="col-md-2">
   </div>
     <div class="col-md-8">
       <h1 class="page-title">Manual Plunging Cryo-EM Grids</h1>
        <p> Cryogenic-electron microscopy (cryo-EM) relies on the imaging of biological samples in aqueous solutions that are flash frozen to form a thin film of “glass-like” ice – a process known as vitrification – that preserves the native biochemical state of the molecule of interest. This process represents a critical aspect of the cryo-EM workflow and is necessary to render the specimen suitable for imaging in the vacuum of the electron microscope. Briefly, a small volume of sample (i.e., 3 µL) is applied to a specialized EM grid (of which there are many types) and excess solution is removed using physical interaction of the EM grid with blotting paper before the grid is quickly plunged into liquid ethane kept at liquid nitrogen temperature. The combination of the thin layer of sample and the high rate of heat transfer in the liquid ethane prevents water molecules from forming crystalline ice, resulting instead in a vitrified layer of liquid with the molecules of interest randomly distributed in it. </p>
        <p> A critical component of freezing samples is the thickness of the vitreous ice film – if the ice is too thick then imaging quality deteriorates dramatically due to increased scattering of the electron beam while ice that is too thin can restrict protein orientations and/or exclude particles from the center of the grid foil holes. Unfortunately, the timing of the blotting process is usually empirically determined for each specimen as sample properties and buffer conditions can alter the behavior during blotting. This reliance on the perfect ice thickness for single-particle cryo-EM has led to a wide array of techniques and equipment that can freeze samples, including robotics, microfluidics, and ultrasonic devices or spraying devices. </p>
        <p> Despite numerous advances in the design of transmission electron microscopes, stability of the electron optics, and advances in data collection and data processing strategies, the methodologies for the vitrification of biological samples for cryo-EM dates back over 40 years and many aspects of this technique, including the equipment that have been developed for this process, rely on the originally detailed “blot-and-plunge” method. Most of the advances in sample preparation since vitrification was introduced have centered around automating the process. While the first implementation involved a simple manual plunger, typically used in a cold room to control temperature and humidity, modern devices (e.g., the ThermoFisher Vitrobot Mark IV, the Gatan Cryoplunge 3, and the Leica EM GP2) are computer-controlled, have enclosed chambers with temperature and humidity control, and have automated most of the process. However, the fundamentals of the steps involved – sample application, blotting, and plunge-freezing – have remained unchanged. </p>
        <p> Some of the most popular sample preparation devices rely on the use of robotics to freeze samples using the blot-and-plunge technique. While these devices are designed to reproducibly create proper ice thickness for imaging, they often remain too expensive for individual labs to purchase and operate and are generally found within cryo-EM facilities at hourly rates for usage. Recently, the original manual blot-and-plunge technique has reappeared as a viable option and a skilled researcher can achieve the same, if not better reproducibility as the robotics mentioned above, at a fraction of the cost, and can easily be owned and operated by individual labs. Manual blotting also offers more users control over blotting as researchers can adjust the type of blotting (i.e. back of the grids, front of the grids), and blotting time based on sample types (single molecules, cells, tissues, etc.) and research questions. Here, we describe the development and implementation of the Mark VI, a cheap and versatile manual plunging platform that allows for the rapid and reproducible freezing of biological specimens using a traditional “blot-and-plunge” style plunger. Each of these components can be easily sourced at low cost and many components can be 3D printed using widely available resources. </p>
     </div>
   <div class="col-md-2">
   </div>
 </div>
</div>

<img class="img-responsive center-block" src="/assets/img/Plunger1.png" width="500" alt="EM">

<div class="container">
 <div class="row">
   <div class="col-md-2">
   </div>
     <div class="col-md-8">
        <p> <b>Figure 1 Traditional “blot-and-plunge” style manual plunger.</b> Diagram showing the manual plunger setup with the Mark VI. The bump stop sets the working height of the tweezers. The pedal pulls on the cable and releases the bar to the working plunge height. The attached tweezers hold the grid during plunging and vitrification. </p>
      </div>
 </div>
</div>
 
<img class="img-responsive center-block" src="/assets/img/Dewar_expload.v1-01.png" alt="EM">
      
<div class="container">
 <div class="row">
   <div class="col-md-2">
   </div>
     <div class="col-md-8">
      <p> <b>Figure 2 Mark VI dewar platform design. </b> Schematic diagram of the Mark VI plunge freezing dewar detailing critical components. The platform base establishes the height of the dewar platform. The Platform Support rests on the Platform Base and houses the Brass Ethane Vessel. The Spinning Grid Storage Platform houses grid boxes for the storage of EM grids that have been prepared and flash frozen. Shown on the <i>left</i> is a design for the use of ethane cryogen and the design on the <i>right</i>, with holes engineered in the Ethane Vessel Holder, is designed to work with a ethane:propane (50:50) mix.  </p>
      </div>
 </div>
</div>
 
<img class="img-responsive center-block" src="/assets/img/cryogen_timecourse.v1-01.png" alt="EM">
      
<div class="container">
 <div class="row">
   <div class="col-md-2">
   </div>
     <div class="col-md-8">
      <p> <b>Figure 3 Cryogen preparation and stability.</b> Timelapse of liquid ethane solidifying over 30 minutes (<i>left</i> panel) before primed for grid freezing. By contrast a 50:50 ethane:propane mix (<i>right</i> panel) remaining in liquid state over the 30 minutes, but primed for grid freezing immediately. </p>
      </div>
 </div>
</div>
 
