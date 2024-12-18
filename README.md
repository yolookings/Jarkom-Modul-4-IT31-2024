# Jarkom-Modul-4-IT31-2024

## Anggota Kelompok IT31 :

| Nama Lengkap         | NRP        |
| -------------------- | ---------- |
| Maulana Ahmad Zahiri | 5027231010 |
| Dzaky Faiq Fayyadhi  | 5027231047 |

## IP PREFIX

`192.232`

## DAFTAR ISI

- [VLSM](#vlsm)

  - [Topology VLSM (Cisco Packet Tracer)](#topology-vlsm-cisco-packet-tracer)
  - [Rute Subnet](#rute-subnet)
  - [VLSM Tree](#vlsm-tree)
  - [Pengurutan Host](#pengurutan-host)

- [CIDR](#cidr)

### Topology VLSM (Cisco Packet Tracer)

![alt text](/img/topology-cisco.png)

### Rute Subnet

| Nama Subnet | Rute                                                                                        | Jumlah IP | Netmask |
| ----------- | ------------------------------------------------------------------------------------------- | --------- | ------- |
| A1          | Holo-Council > Switch12                                                                     | 62        | /26     |
| A2          | Hololive > HoloEN > Holo-Myth > HoloPromise > Router15 > Tys                                | 3         | /29     |
| A3          | Hololive > HoloEN > Holo-Myth > HoloPromise > Router15 > Holo-Council                       | 3         | /29     |
| A4          | Hololive > HoloEN > HoloAdvent > SW10 > FuwaMoco, Shiori_Nerissa, Biboo                     | 28        | /27     |
| A5          | Hololive > Holo-EN > Holo-Myth > SW9 > Gura_Ama_Ina > Kiara_Calli                           | 503       | /23     |
| A6          | Hololive > HoloEN > Holo-Myth > HoloPromise > Holo-Council > SW12 > Kronii_Mumei, Bae_Fauna | 2         | /30     |
| A7          | Hololive > HoloEN > HoloAdvent                                                              | 14        | /28     |
| A8          | Hololive > Holo-JP > SW1 > DEV_IS > Re:GLO$$ > Ririka_Raden, Ao, Hajime_Kanade              | 2         | /30     |
| A9          | Hololive > Holo-EN                                                                          | 2         | /30     |
| A10         | Hololive > Holo-JP                                                                          | 2         | /30     |
| A11         | Hololive > Holo-JP > SW1 > DEV_IS, GEN:0                                                    | 3         | /29     |
| A12         | Hololive > Holo-JP > SW1 > DEV_IS, GEN:0 > SW5 > GEN:1 > GAMERS > SW8 > Korone, Okayu, Mio  | 2         | /30     |
| A13         | Hololive > Holo-ID                                                                          | 120       | /25     |
| A14         | Hololive > Holo-ID > SW2 > AREA15 > Moona, Bisu, lofi                                       | 661       | /22     |
| A15         | Hololive > Holo-ID > AREA 15                                                                | 2         | /30     |
| A16         | Hololive > Holo-ID > holoro                                                                 | 2         | /30     |
| A17         | Hololive > Holo-ID > holoh3ro                                                               | 2         | /30     |
| A18         | Hololive > Holo-JP > SW1 > DEV_IS, GEN:0 > SW5 > MiComet, Sora_Robo_AZki, GEN:1             | 2045      | /21     |
| A19         | Hololive > Holo-JP > SW1 > DEV_IS, GEN:0 > SW5 > GEN:1 > GAMERS                             | 2         | /30     |
| A20         | Hololive > Holo-ID > holoro > SW3, Ollie, Anya, Reine                                       | 34        | /26     |
| A21         | Hololive > Holo-ID > holoh3ro > SW4 > Zeta, Kaela, Kobo                                     | 299       | /23     |
| A22         | Hololive > Holo-JP > SW1 > DEV_IS, GEN:0 > SW5 > GEN:1 > Member > PBK_Matsuri, Aki_Hachama  | 470       | /23     |
| TOTAL       |                                                                                             | 4263      | /19     |

### VLSM Tree

![alt text](/img/vlsm-tree.png)

### Pengurutan Host

- `(Dari Terbesar ke Terkecil)`

1. A14 (661 host) - /22
2. A18 (2045 host) - /21
3. A22 (470 host) - /23
4. A21 (299 host) - /23
5. A1 (62 host) - /26
6. A5 (503 host) - /23
7. A13 (120 host) - /25
8. A20 (34 host) - /26
9. A7 (14 host) - /28
10. A4 (28 host) - /27
11. A2, A3, A11 (3 host masing-masing) - /29
12. A6, A8, A9, A10, A12, A15, A16, A17, A19 (2 host masing-masing) - /30

### 2. Tabel Pembagian IP VLSM

| Subnet | Host | Prefix | Length | Subnet Mask     | Network ID     | IP Awal        | IP Akhir       | Broadcast      |
| ------ | ---- | ------ | ------ | --------------- | -------------- | -------------- | -------------- | -------------- |
| A18    | 2045 | /21    | 2048   | 255.255.248.0   | 192.232.0.0    | 192.232.0.1    | 192.232.7.254  | 192.232.7.255  |
| A14    | 661  | /22    | 1024   | 255.255.252.0   | 192.232.8.0    | 192.232.8.1    | 192.232.11.254 | 192.232.11.255 |
| A22    | 470  | /23    | 512    | 255.255.254.0   | 192.232.12.0   | 192.232.12.1   | 192.232.13.254 | 192.232.13.255 |
| A21    | 299  | /23    | 512    | 255.255.254.0   | 192.232.14.0   | 192.232.14.1   | 192.232.15.254 | 192.232.15.255 |
| A5     | 503  | /23    | 512    | 255.255.254.0   | 192.232.16.0   | 192.232.16.1   | 192.232.17.254 | 192.232.17.255 |
| A12    | 120  | /25    | 128    | 255.255.255.128 | 192.232.18.0   | 192.232.18.1   | 192.232.18.126 | 192.232.18.127 |
| A1     | 62   | /26    | 64     | 255.255.255.192 | 192.232.18.128 | 192.232.18.29  | 192.232.18.190 | 192.232.18.191 |
| A20    | 34   | /26    | 64     | 255.255.255.192 | 192.232.18.192 | 192.232.18.193 | 192.232.18.254 | 192.232.18.255 |
| A4     | 28   | /27    | 32     | 255.255.255.224 | 192.232.19.0   | 192.232.19.1   | 192.232.19.30  | 192.232.19.31  |
| A8     | 14   | /28    | 16     | 255.255.255.240 | 192.232.19.32  | 192.232.19.33  | 192.232.19.46  | 192.232.19.47  |
| A2     | 3    | /29    | 8      | 255.255.255.248 | 192.232.19.48  | 192.232.19.49  | 192.232.19.54  | 192.232.19.55  |
| A3     | 3    | /29    | 8      | 255.255.255.248 | 192.232.19.56  | 192.232.19.57  | 192.232.19.62  | 192.232.19.63  |
| A11    | 3    | /29    | 8      | 255.255.255.248 | 192.232.19.64  | 192.232.19.65  | 192.232.19.70  | 192.232.19.71  |
| A6     | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.72  | 192.232.19.73  | 192.232.19.74  | 192.232.19.75  |
| A7     | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.76  | 192.232.19.77  | 192.232.19.78  | 192.232.19.79  |
| A9     | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.80  | 192.232.19.81  | 192.232.19.82  | 192.232.19.83  |
| A10    | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.84  | 192.232.19.85  | 192.232.19.86  | 192.232.19.87  |
| A13    | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.88  | 192.232.19.89  | 192.232.19.90  | 192.232.19.91  |
| A15    | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.92  | 192.232.19.93  | 192.232.19.94  | 192.232.19.95  |
| A16    | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.96  | 192.232.19.97  | 192.232.19.98  | 192.232.19.99  |
| A17    | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.100 | 192.232.19.101 | 192.232.19.102 | 192.232.19.103 |
| A19    | 2    | /30    | 4      | 255.255.255.252 | 192.232.19.104 | 192.232.19.105 | 192.232.19.106 | 192.232.19.107 |
