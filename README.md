<h2 align="center">⚡⚡ArcProject⚡⚡</h2>

<p align="center">
<img src="images/Imagem-Reator-Homem-de-Ferro-PNG.png" width="150" alt="accessibility text">
</p>
<p align="center"The project Arc is a agglomerate of repositories write with Julia, Python and R for the study of nuclear reactors.
</p>
<h2 align="center">PIN-CELL</h2>
<br>
The first reactor I will simulate is a pin cell reactor, the smallest unit of a nuclear reactor, in this case I will use scripts from Julia to modelling a neutron transport phenomenon for the control volume. 
Where I defined the number of azimutal angles (nφ) as 32, the azimutal spacing (δ) as 0.001, the boundary conditions as reflective and with these conditions will be setted into the TrackGenerator() method to generate the Tracks:
<br> 
<p align="center">
<img src="pincell-tracks.png" width="350" alt="accessibility text">
</p>
A variable called "tr" will get the method TrackGenerator() to proceed the segmentation with the function segmentize!(tg):
<p align="center">
  <img src="images/pincell-segments.png" width="350" alt="accessibility text">
  </p>
  
 After doing this, the next step is setting the variables for the reactor material the pin-fuel, water for cooling and the cladding:
 <br>
 <p align="center">PIN
 <br>
    νΣf = [1.86278e-2, 3.44137e-1]
    <br>
    Σt  = [3.62022e-1, 5.72155e-1]
    <br>
    Σs0 = [3.33748e-1  6.64881e-4; 0.0e-0 3.80898e-1]
    <br>

</p>
     <p align="center">CLADDING
  <br>
    Σt  = [2.74144e-1, 2.80890e-1]
    <br>
    Σs0 = [2.72377e-1 1.90838e-4; 0.0e-0 2.77230e-1]
<br>
</p>
 <p align="center">WATER
  <br>
Σt  = [6.40711e-1, 1.69131e-0]
    <br>
    Σs0 = [6.07382e-1 3.31316e-2; 0.0e-0 1.68428e-0]
</p>
<br>
With the material variables defined the next step is to use the solve method and write a vtk type of file, a typical one for simulated geometries. 
