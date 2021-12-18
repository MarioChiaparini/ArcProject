<h2>ArcProject</h2>

<p>The project Arc is a agglomerate of repositories write with Julia, Python and R for the study of nuclear reactors.
</p>
<br>
<br>
<center><h2>PIN-CELL</h2></center>
<br>
The first reactor I will simulate will be a pin cell reactor, the smallest unit of a reactor, in this case I will use scripts from Julia to modelling a neutron trnasport for the control volume. 
Where I defined the number of azimutal angles (nφ) as 32, the azimutal spacing (δ) as 0.001, the boundary conditions as reflective and with these conditions will be setted into the TrackGenerator() method to generate the Tracks:
<br> 
<img src="pincell-tracks.png" width="350" alt="accessibility text">
