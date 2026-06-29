# CPU_DATA column dictionary
---

## Per-core columns `C{n}_…` (n = core index 0–7)

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `C{n}_T` | Core n temperature *(Core{n} (CCD1), °C)* |
| `C{n}_P` | Core n power *(Core n Power, W)* |
| `C{n}_R` | Core n ratio = clock multiplier *(Core n Ratio)* |
| `C{n}_VID` | Core n VID = requested voltage ID *(Core n VID, V)* |
| `C{n}_Clk` | Core n clock *(Core n Clock (perf #k), MHz)* — `perf #k` is OCCT's best-core ranking (#1 = fastest), not the core index |
| `C{n}_C0res` | Core n C0-state (active) residency *(Core n C0 Residency, %)* |
| `C{n}_C1res` | Core n C1-state (idle) residency *(Core n C1 Residency, %)* |
| `C{n}_C6res` | Core n C6-state (deep sleep) residency *(Core n C6 Residency, %)* |
| `C{n}_T0_EClk` | Core n thread 0 effective clock *(Core n T0 Effective Clock, MHz)* |
| `C{n}_T1_EClk` | Core n thread 1 effective clock *(Core n T1 Effective Clock, MHz)* |
| `C{n}_T0_U` | Core n thread 0 usage *(Core n T0 Usage, %)* |
| `C{n}_T1_U` | Core n thread 1 usage *(Core n T1 Usage, %)* |
| `C{n}_T0_Util` | Core n thread 0 utility *(Core n T0 Utility, %)* |
| `C{n}_T1_Util` | Core n thread 1 utility *(Core n T1 Utility, %)* |


---

## CPU package temperatures

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `CPU_Tctl` | CPU control temperature *(CPU (Tctl/Tdie), °C)* |
| `CPU_DieAvg` | CPU die average temperature *(CPU Die (average), °C)* |
| `CCD1_Tdie` | CCD1 (core-complex die) temperature *(CPU CCD1 (Tdie), °C)* |
| `IOD_Avg` | I/O die average temperature *(CPU IOD Average, °C)* |
| `IOD_Hot` | I/O die hotspot temperature *(CPU IOD Hotspot, °C)* |
| `L3_T` | L3 cache temperature *(L3 Cache (CCD1), °C)* |

## CPU power

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `CPU_PPT` | Package Power Tracking — total socket power *(CPU PPT, W)* |
| `CPU_Pkg_P` | CPU package power *(CPU Package Power, W)* |
| `CPU_Core_P` | CPU core-rail power, SVI3 telemetry *(CPU Core Power (SVI3 TFN), W)* |
| `CPU_SoC_P` | SoC power *(CPU SoC Power (SVI3 TFN), W)* |
| `CPU_Tot_P` | Core + SoC + MISC total power *(Core+SoC+MISC Power (SVI3 TFN), W)* |

## CPU current

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `CPU_Core_I` | CPU core-rail current *(CPU Core Current (SVI3 TFN), A)* |
| `CPU_SoC_I` | SoC current *(SoC Current (SVI3 TFN), A)* |
| `CPU_MISC_I` | MISC-rail current *(MISC Current (SVI3 TFN), A)* |
| `CPU_TDC` | Thermal Design Current *(CPU TDC, A)* |
| `CPU_EDC` | Electrical Design Current (peak) *(CPU EDC, A)* |

## Clocks

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `Avg_EClk` | Average effective clock across cores *(Average Effective Clock, MHz)* |
| `Bus_Clk` | Reference bus clock *(Bus Clock, MHz)* |
| `FCLK` | Infinity Fabric clock *(Infinity Fabric Clock (FCLK), MHz)* |
| `UCLK` | Memory-controller clock *(Memory Controller Clock (UCLK), MHz)* |
| `L3_Clk` | L3 cache clock *(L3 Cache (CCD1), MHz)* |
| `Freq_GLim` | Global frequency limit *(Frequency Limit - Global, MHz)* |

## Usage / activity

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `CPU_U` | Total CPU usage *(Total CPU Usage, %)* |
| `CPU_Util` | Total CPU utility (work-normalized load) *(Total CPU Utility, %)* |
| `MaxThr_U` | Highest single core/thread usage *(Max CPU/Thread Usage, %)* |
| `AvgActC` | Average number of active cores *(Average Active Core Count)* |
| `Pkg_C6` | Package C6 (deep sleep) residency *(Package C6 Residency, %)* |

## Limits reached (% of the cap currently being hit)

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `PPT_Lim` | % of PPT power limit *(CPU PPT Limit, %)* |
| `PPT_F_Lim` | % of PPT FAST limit *(CPU PPT FAST Limit, %)* |
| `TDC_Lim` | % of TDC current limit *(CPU TDC Limit, %)* |
| `EDC_Lim` | % of EDC current limit *(CPU EDC Limit, %)* |
| `T_Lim` | % of thermal limit *(Thermal Limit, %)* |

## Throttling flags

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `HTC_TT` | Hardware Thermal Control throttling active *(Thermal Throttling (HTC))* |
| `PROCHOT_CPU` | PROCHOT (internal) throttling active *(Thermal Throttling (PROCHOT CPU))* |
| `PROCHOT_EXT` | PROCHOT (external) throttling active *(Thermal Throttling (PROCHOT EXT))* |

## Voltages and VRM temperatures

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `VDDCR_VDD_V` | Core (VDDCR_VDD) rail voltage *(CPU VDDCR_VDD Voltage (SVI3 TFN), V)* |
| `VDDCR_SOC_V` | SoC (VDDCR_SOC) rail voltage *(CPU VDDCR_SOC Voltage (SVI3 TFN), V)* |
| `VDD_MISC_V` | MISC rail voltage *(CPU VDD_MISC Voltage (SVI3 TFN), V)* |
| `VDDCR_VDD_TVRM` | Core-rail VRM temperature *(CPU VDDCR_VDD VRM (SVI3 TFN), °C)* |
| `VDDCR_SOC_TVRM` | SoC-rail VRM temperature *(CPU VDDCR_SOC VRM (SVI3 TFN), °C)* |
| `VDD_MISC_TVRM` | MISC-rail VRM temperature *(CPU VDD_MISC VRM (SVI3 TFN), °C)* |

## Memory bandwidth (reported under the CPU/IOD)

| Column | Meaning *(OCCT full name, unit)* |
|---|---|
| `DRAM_R_BW` | DRAM read bandwidth *(DRAM Read Bandwidth)* |
| `DRAM_W_BW` | DRAM write bandwidth *(DRAM Write Bandwidth)* |
