# Open-ghost-cam-
Multispectral coherence Cam 
# OpenGhostCam  
**An open-source UV/EMF anomaly detector using 40Hz phase coherence validation.**  

![Prototype Image](images/ghostcam_proto.jpg) *[Blurred or angled photo—no close-ups of coils]*  

## **Key Features**  
- **UV Sensor:** Sony IMX487 with 40Hz LCTF (300–450nm)  
- **EMF Array:** TriField-compatible 3-axis magnetometer  
- **DSP Core:** Artix-7 FPGA validates cross-sensor anomalies  
- **Open-Source:** Schematics, firmware, and 3D-printable case  

## **Hardware Schematic**  
![Block Diagram](images/safe_block_diagram.png)  

### **Sanitized Block Diagram**  
```plaintext  
[UV Lens] → [40Hz LCTF] → [IMX487] → [I2C]  
                                      ↓  
[TriField EMF] → [ADC] → [Artix-7 FPGA] → [MicroSD/Bluetooth]  
                                      ↑  
[19.8Hz MEMS Mic] → [Bandpass Filter]  
