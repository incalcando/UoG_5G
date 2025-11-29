Required libaries for Pd:

- aoo
- osc
- hcs

best to load from Deken


Usage:

Load patch <b>UoG_5G_main.pd</b> on one of the computers (this will be most likely be the computer most consistently being used in the project:
The Rapsberry Pi 5 prototype with audio card connected to audio equipment.

All computers involved will need to load the patch <b>UoG_5G_user.pd</b> patch.

URGENT TODO:

text transmission did not seem to work from mac to pi.
- test pi to pi,
- redo test from mac to mac, which had worked before.

  TODO:

  - automatic port association dependent on no of users/peers and audio streams.
  - text transmission required to 'publish' available track names/content for connected peers to choose from.


transfer test using iperf3

on Linux (raspbian):
sudo apt update
sudo apt install iperf3

on macOS:
brew install iperf3

run 
<code>iperf3 -s </code>
on one and
iperf3 -c <pi-ip-address> -t 10

or better for udp simulation: (udo -u)
iperf3 -c <pi-ip-address> -u -b 20M





  used networkquality -v in terminal to measure G5 speed when connecting to access point in Uni:
  networkquality -v

results need proper checking, but numbers should suggest that speed should be fine for 11/12 stereo channels of audio.
  
Downlink: capacity 0.000 Mbps, responsiveness 0 RPM (0 B, 0 flows) - Uplink: capDownlink: capacity 9.641 Mbps, responsiveness 0 RPM (247.608 KB, 1 flows) - UpliDownlink: capacity 66.406 Mbps, responsiveness 0 RPM (3.328 MB, 1 flows) - UplinDownlink: capacity 137.017 Mbps, responsiveness 0 RPM (11.609 MB, 1 flows) - UplDownlink: capacity 199.715 Mbps, responsiveness 0 RPM (22.295 MB, 1 flows) - UplDownlink: capacity 220.246 Mbps, responsiveness 0 RPM (30.389 MB, 1 flows) - UplDownlink: capacity 246.730 Mbps, responsiveness 0 RPM (39.887 MB, 2 flows) - UplDownlink: capacity 248.590 Mbps, responsiveness 1215 RPM (46.497 MB, 2 flows) - Downlink: capacity 262.933 Mbps, responsiveness 1214 RPM (56.418 MB, 2 flows) - Downlink: capacity 274.103 Mbps, responsiveness 1191 RPM (66.089 MB, 2 flows) - Downlink: capacity 283.764 Mbps, responsiveness 1169 RPM (76.339 MB, 3 flows) - Downlink: capacity 291.822 Mbps, responsiveness 1156 RPM (85.665 MB, 3 flows) - Downlink: capacity 295.751 Mbps, responsiveness 1139 RPM (94.626 MB, 3 flows) - Downlink: capacity 304.796 Mbps, responsiveness 1121 RPM (104.993 MB, 3 flows) -Downlink: capacity 318.293 Mbps, responsiveness 1103 RPM (117.648 MB, 3 flows) -Downlink: capacity 324.183 Mbps, responsiveness 1088 RPM (127.931 MB, 4 flows) -Downlink: capacity 321.473 Mbps, responsiveness 1078 RPM (135.199 MB, 4 flows) -Downlink: capacity 328.961 Mbps, responsiveness 1067 RPM (147.056 MB, 4 flows) -Downlink: capacity 338.845 Mbps, responsiveness 1057 RPM (159.755 MB, 4 flows) -Downlink: capacity 343.017 Mbps, responsiveness 1048 RPM (170.223 MB, 4 flows) -Downlink: capacity 345.778 Mbps, responsiveness 1038 RPM (180.191 MB, 5 flows) -Downlink: capacity 365.137 Mbps, responsiveness 1038 RPM (190.113 MB, 5 flows) -Downlink: capacity 378.656 Mbps, responsiveness 1027 RPM (199.970 MB, 5 flows) -Downlink: capacity 385.397 Mbps, responsiveness 1018 RPM (210.298 MB, 5 flows) -Downlink: capacity 385.283 Mbps, responsiveness 1010 RPM (219.938 MB, 5 flows) -Downlink: capacity 389.930 Mbps, responsiveness 1002 RPM (229.828 MB, 6 flows) -Downlink: capacity 389.461 Mbps, responsiveness 993 RPM (239.107 MB, 6 flows) - Downlink: capacity 396.238 Mbps, responsiveness 983 RPM (248.998 MB, 6 flows) - Downlink: capacity 397.442 Mbps, responsiveness 960 RPM (258.719 MB, 6 flows) - Downlink: capacity 394.341 Mbps, responsiveness 936 RPM (266.852 MB, 6 flows) - Downlink: capacity 395.956 Mbps, responsiveness 913 RPM (277.319 MB, 7 flows) - Downlink: capacity 400.846 Mbps, responsiveness 892 RPM (289.120 MB, 7 flows) - Downlink: capacity 402.091 Mbps, responsiveness 869 RPM (298.261 MB, 7 flows) - Downlink: capacity 401.420 Mbps, responsiveness 869 RPM (308.276 MB, 7 flows) - Downlink: capacity 402.130 Mbps, responsiveness 848 RPM (321.009 MB, 7 flows) - Downlink: capacity 403.184 Mbps, responsiveness 828 RPM (332.134 MB, 8 flows) - Downlink: capacity 409.718 Mbps, responsiveness 809 RPM (342.469 MB, 8 flows) - Downlink: capacity 407.549 Mbps, responsiveness 789 RPM (352.646 MB, 8 flows) - Downlink: capacity 399.837 Mbps, responsiveness 768 RPM (361.463 MB, 8 flows) - Downlink: capacity 396.173 Mbps, responsiveness 768 RPM (370.148 MB, 8 flows) - Downlink: capacity 395.748 Mbps, responsiveness 725 RPM (382.013 MB, 9 flows) - Downlink: capacity 399.979 Mbps, responsiveness 725 RPM (394.161 MB, 9 flows) - Downlink: capacity 406.702 Mbps, responsiveness 702 RPM (407.875 MB, 9 flows) - Downlink: capacity 399.711 Mbps, responsiveness 680 RPM (414.063 MB, 9 flows) - Downlink: capacity 394.443 Mbps, responsiveness 658 RPM (420.905 MB, 9 flows) - Downlink: capacity 398.072 Mbps, responsiveness 636 RPM (434.145 MB, 10 flows) -Downlink: capacity 392.295 Mbps, responsiveness 613 RPM (440.433 MB, 10 flows) -Downlink: capacity 398.567 Mbps, responsiveness 589 RPM (454.517 MB, 10 flows) -Downlink: capacity 403.726 Mbps, responsiveness 567 RPM (468.131 MB, 10 flows) -Downlink: capacity 404.327 Mbps, responsiveness 546 RPM (478.673 MB, 10 flows) -Downlink: capacity 404.275 Mbps, responsiveness 527 RPM (488.745 MB, 11 flows) -Downlink: capacity 402.892 Mbps, responsiveness 527 RPM (497.797 MB, 11 flows) -Downlink: capacity 394.320 Mbps, responsiveness 509 RPM (501.013 MB, 11 flows) -Downlink: capacity 404.298 Mbps, responsiveness 492 RPM (519.247 MB, 11 flows) -Downlink: capacity 397.853 Mbps, responsiveness 475 RPM (524.008 MB, 11 flows) -Downlink: capacity 403.690 Mbps, responsiveness 457 RPM (539.313 MB, 12 flows) -Downlink: capacity 403.701 Mbps, responsiveness 441 RPM (549.419 MB, 12 flows) -Downlink: capacity 403.680 Mbps, responsiveness 425 RPM (559.497 MB, 12 flows) -Downlink: capacity 403.713 Mbps, responsiveness 409 RPM (569.640 MB, 12 flows) -Downlink: capacity 404.228 Mbps, responsiveness 393 RPM (580.418 MB, 12 flows) -Downlink: capacity 397.462 Mbps, responsiveness 378 RPM (583.842 MB, 13 flows) -Downlink: capacity 395.556 Mbps, responsiveness 364 RPM (591.882 MB, 13 flows) -Downlink: capacity 402.841 Mbps, responsiveness 364 RPM (609.949 MB, 13 flows) -Downlink: capacity 403.142 Mbps, responsiveness 351 RPM (620.349 MB, 13 flows) -Downlink: capacity 402.832 Mbps, responsiveness 338 RPM (630.323 MB, 13 flows) -Downlink: capacity 402.957 Mbps, responsiveness 327 RPM (640.574 MB, 14 flows) -Downlink: capacity 402.555 Mbps, responsiveness 315 RPM (650.197 MB, 14 flows) -Downlink: capacity 402.616 Mbps, responsiveness 305 RPM (660.351 MB, 14 flows) -Downlink: capacity 402.267 Mbps, responsiveness 295 RPM (669.999 MB, 14 flows) -Downlink: capacity 402.269 Mbps, responsiveness 286 RPM (680.058 MB, 14 flows) -Downlink: capacity 399.102 Mbps, responsiveness 276 RPM (686.162 MB, 15 flows) -Downlink: capacity 392.790 Mbps, responsiveness 267 RPM (688.139 MB, 15 flows) -Downlink: capacity 402.077 Mbps, responsiveness 257 RPM (710.033 MB, 15 flows) -Downlink: capacity 401.634 Mbps, responsiveness 247 RPM (719.559 MB, 15 flows) -Downlink: capacity 394.536 Mbps, responsiveness 238 RPM (720.019 MB, 15 flows) -Downlink: capacity 394.128 Mbps, responsiveness 230 RPM (729.363 MB, 16 flows) -Downlink: capacity 401.599 Mbps, responsiveness 230 RPM (749.684 MB, 16 flows) -Downlink: capacity 394.910 Mbps, responsiveness 223 RPM (750.211 MB, 16 flows) -Downlink: capacity 391.190 Mbps, responsiveness 216 RPM (754.766 MB, 16 flows) -Downlink: capacity 402.143 Mbps, responsiveness 210 RPM (780.767 MB, 16 flows) -Downlink: capacity 397.935 Mbps, responsiveness 204 RPM (784.522 MB, 16 flows) -Downlink: capacity 391.803 Mbps, responsiveness 199 RPM (785.118 MB, 16 flows) -Downlink: capacity 403.155 Mbps, responsiveness 194 RPM (812.545 MB, 16 flows) -Downlink: capacity 399.828 Mbps, responsiveness 190 RPM (817.486 MB, 16 flows) -Downlink: capacity 393.657 Mbps, responsiveness 190 RPM (817.612 MB, 16 flows) -Downlink: capacity 397.196 Mbps, responsiveness 185 RPM (833.381 MB, 16 flows) -Downlink: capacity 402.007 Mbps, responsiveness 181 RPM (851.267 MB, 16 flows) -Downlink: capacity 397.027 Mbps, responsiveness 177 RPM (852.988 MB, 16 flows) -Downlink: capacity 392.591 Mbps, responsiveness 174 RPM (855.381 MB, 16 flows) -Downlink: capacity 401.998 Mbps, responsiveness 170 RPM (882.023 MB, 16 flows) -Downlink: capacity 400.446 Mbps, responsiveness 167 RPM (889.636 MB, 16 flows) - Uplink: capacity 26.064 Mbps, responsiveness 167 RPM (57.249 MB, 16 flows)^C
sebastian@SL-macBook ~ % 
