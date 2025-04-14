# Setup (Edition 2025)

## Misc

:material-cloud: Internet

| Provider         | Plan             | Speed                                 |
|------------------|------------------|---------------------------------------|
| Bouygues Telecom | B&You Pure Fibre | :arrow_down: 8Gb/s :arrow_up: 1 Gb/s |

## Baremetal Servers

:material-server: `bm1.bunbun.ovh`

| Component    | Name                             |
|--------------|----------------------------------|
| Barebone     | Dell OptiPlex 7050 Micro         |
| CPU          | Intel Core i7-7700T (4C/8T, 35W) |
| RAM          | 2x16GB SO-DIMM DDR4 2133Mhz      |
| SSD (System) | Crucial BX500 240GB              |
| NVMe (Data)  | 1TB PCIe Gen3                    |

:material-server: `bm2.bunbun.ovh`

| Component    | Name                              |
|--------------|-----------------------------------|
| Barebone     | Lenovo M920q                      |
| CPU          | Intel Core i7-8700T (6C/12T, 35W) |
| RAM          | 2x16GB SO-DIMM DDR4 2666Mhz       |
| SSD (System) | 240GB                             |
| NVMe (Data)  | 1TB PCIe Gen3                     |

:material-server: `bm3.bunbun.ovh`

| Component    | Name                              |
|--------------|-----------------------------------|
| Barebone     | Lenovo M920q                      |
| CPU          | Intel Core i7-8700T (6C/12T, 35W) |
| RAM          | 1x16GB SO-DIMM DDR4 2666Mhz       |
| SSD (System) | 240GB                             |
| NVMe (Data)  | ---                               |

## Network Attached Storage

:material-server: `nas.bunbun.ovh`

| Component     | Name                                                       |
|---------------|------------------------------------------------------------|
| Case          | Jonsbo N4                                                  |
| PSU           | Corsair SF750                                              |
| MBD           | MSI B450M Mortar Titanium                                  |
| CPU           | AMD Ryzen 5 5600X (6C/12T, 65W)                            |
| CPU (Cooler)  | Noctua NH-L9a-AM4                                          |
| RAM           | Corsair Vengeance RGB RS 2x16GB DDR4 3200Mhz               |
| GPU           | Sparkle Intel Arc 310 4GB GDDR6                            |
| Pool 1 (Boot) | 2x Patriot Elite Burst 240GB 2.5¨                          |
| Pool 2 (Data) | 2x Seagate IronWolf NAS 4TB 3.5¨ (ST4000VN006/ST4000VN008) |
| Pool 3 (VMs)  | 1x WD Blue SN550 500GB 2280 PCIe Gen3                      |

## Retired Devices

:material-server-off: Raspberry Pi 3B 1GB

:material-server-off: Synology DS214play