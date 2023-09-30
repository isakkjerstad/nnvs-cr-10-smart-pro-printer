# Files:
- CR-10_Smart_Pro.curaprofile -> Cura profile for high quality printing with the printer.
- profile.3mf -> Machine settings and profile for the printer.

## CR-10 Smart Pro settings:
### Printer Settings:
- **X (Width):** 300.0 mm
- **Y (Depth):** 300.0 mm
- **Z (Height):** 400.0 mm
- **Build plate shape:** Rectangular
- **Origin at center:** No
- **Heated bed:** Yes
- **Heated build volume:** No
- **G-code flavor:** Marlin

### Printhead Settings:
- **X min:** -26 mm
- **Y min:** -32 mm
- **X max:** 32 mm
- **Y max:** 34 mm
- **Gantry height:** 25.0 mm
- **Number of extruders:** 1
- **Apply extruder offset to G-code:** Yes

## Nozzle settings:
- **Nozzle size:** 0.4 mm
- **Compatible material diameter:** 1.75 mm
- **Nozzle offset X:** 0 mm
- **Nozzle offset Y:** 0 mm
- **Cooling fan number:** 0

### Start G-code:
```g-code
M201 X500.00 Y500.00 Z100.00 E5000.00;
M203 X500.00 Y500.00 Z10.00 E50.00;
M204 P500.00 R1000.00 T500.00;
M205 X8.00 Y8.00 Z0.40 E5.00;
M220 S100;
M221 S100;

G28;
G29;
M420 S1;

G92 E0;
G1 Z2.0 F3000;
G1 X10.1 Y20 Z0.28 F5000.0;
G1 X10.1 Y200.0 Z0.28 F1500.0 E15;
G1 X10.4 Y200.0 Z0.28 F5000.0;
G1 X10.4 Y20 Z0.28 F1500.0 E30;
G92 E0;
G1 Z2.0 F3000;
```

### End G-code:
```g-code
G91;
G1 E-2 F2700;
G1 E-2 Z0.2 F2400;
G1 X5 Y5 F3000;
G1 Z10;
G90;

G1 X0 Y0;
M106 S0;
M104 S0;
M140 S0;

M64 X Y E;
```

## Warning:
Only use this repository with the **CR-10 Smart Pro** 3D-printer.
