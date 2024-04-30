# Solar-Panel-Control-using-IOT
Controlling the solar panel direction to have maximum output by implementing light tracking using IOT

In this project we are using IOT to have maximun output by solar pannel through light tracking.

The material required are:-

Solar Pannel (https://www.amazon.in/Electronicspices-Solar-Square-Shape-6V-100/dp/B082FHLXBM?pd_rd_w=PKFdz&content-id=amzn1.sym.6aee2dcc-1b4f-45dc-b930-832b2221cce0&pf_rd_p=6aee2dcc-1b4f-45dc-b930-832b2221cce0&pf_rd_r=VQE5MTNKQYKBGA3Z02WF&pd_rd_wg=0Rpfs&pd_rd_r=9332900b-15ef-4d81-9cfc-707fac773329&pd_rd_i=B082FHLXBM&ref_=pd_bap_d_grid_rp_0_1_ec_nped_pd_nav_hcs_rp_1_t&th=1), Quantity-02.
Connect the Solar panel in series for the 12VDC output.

Boost Converter (https://www.amazon.in/XL6009-DC-DC-Converter-Adjustable-Module/dp/B09DBRHV19/ref=sr_1_5?dib=eyJ2IjoiMSJ9.indeghCpJKsUFG1c-aRBzV9NgYs2jq3kY8mw3i8OIwKV6wXPqmRESQLffpqXmFTo-sa6hEQDPtGAk3ZH0JzSl63ilBqYr8vfPHELl67CKJSoh0BT2EgZB1AB8r0WExsYxyVZ-43xdEGOfwV1DHBMSAXT10xpE6VHWdM27CRMrcdleK_eeSeVL0vykaIOnFIZoQUff4ZOKxYJgcfqPc-NLWjd3rKnkx0QxBu7HbePrFU.6OKbkbeRIfQblV2mSEE5oM9G7xnMVRhzzAjJMn0m36g&dib_tag=se&keywords=Boost+converter&qid=1714438671&sr=8-5), Quantity-01.
Connect the Boost converter in series with the solar pannel, this helps to increase the output voltage. Because under load the solar panel does not provide sufficient voltage, which can cause drawing more voltage then required due to which solar panel may get maulfunction.

Charging Module (https://www.amazon.in/gp/product/B08CCCJ7HN/ref=ox_sc_act_title_3?smid=A3OFE3UKIO43OW&psc=1) Quantity-01.
Here I am using Lithium Ions Battery, to charge and discharge this is sufficient. It has max of 12VDC, 10A. This is connected in such a way that Boost converter is in series & parallel with the Lithium Ion Battery. On this module the Boost coverter O/P & the I/P of the Load are connected on the same terminal (P+ for positive & P- for negative). Importantly connect a Diode(1N4001) in series between the Boost converter and Charging Module (Cathode at Cahrging Module & Anode at Boost Converter), to prevent backflow of voltage from battery to boost converter, which can damage the boost converter. This charging module has 4 connection for the connection of the battery, such that B1 for 3.3v, B2 for 7.7v, B3 for 12v or vise versa & B- for GND.

Buck Converter (https://www.amazon.in/LM2596-DC-DC-Buck-Converter-Module/dp/B009P04YTO/ref=sr_1_3_mod_primary_new?crid=ZAUEGKE0TGQC&dib=eyJ2IjoiMSJ9.PkCTOm5yVoM-BBo3_V-uCDcJGJIrux6SrUN53aEDDdZ88rEjghFJJLoRbBy1ICma34bVXpUQCQcy_-fMfv0ECHb3CmbNbeqcRTxRYTZTgUo9aGfDAzepIRHNparQzh1U0ngu_wVMTyFYOcaJO_u_IaxiGscRGGWLgaJcRND03Y2HsnUEcmmYQTAPR0s37E9PMB5iKTEHM9yINesCbp2efdNqpTCVj807Yv5SrSFSb4nrENKr9XKsPb2ViD7FYw5Gkf0dPA6Mcv9g_II9-dHloFIFhWexVXqYJ5sJOExIwG4.e3t_9fPL1hFo8nczZIdzaHNCQ1kn2VibuXPPGdarQUA&dib_tag=se&keywords=buck+converter&qid=1714440341&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=Buck+co%2Caps%2C305&sr=8-3), Quantity-01.
Helps to increase the current of 3Amp with the constant 12VDC output. Connect it in series with the Charging Module.

Inverter (https://www.amazon.in/gp/product/B07MGRQW93/ref=ox_sc_act_title_4?smid=AH017Z3M1ZJ3T&psc=1), Quantity-01.
Convert the DC supply to AC supply. Connect DC terminal in series with the O/P of Buck Converter. Be careful while connecting, since it has 2 terminal i.e one for I/P DC & another O/P AC.

Load (https://www.amazon.in/HAVELLS-Adore-9W-LED-Bulb/dp/B08BYJLB4Z/ref=sr_1_6?crid=3ET61V5EEUL1I&dib=eyJ2IjoiMSJ9.zhu1yXwZn8Y3hmqMROOyP0wx275OkduzIYsEcocsRghiH61SzNOppCcn7iryP9P78ZpQ6M6hRpxh5rL3Qg0vhbjENMeZAaathV-BtycIuKxPozeET7goVquT_pQua4N9E1MXgQ-dPII2MBKn6j5ehhjQcGfVAqwtywaV5OOz76Ioj2HkiQd2cd_FL5_DtX-HijSf9LxvrvqxH87v2IckSApC6aPfSvgTt9oRE24e3r0Jj5upyBDaKDms_rDufy2oN5OzRcbsv5gNcXBtcq0j9mxKYD8iA_2s-bacRH5nsJ8.2SJZF7PtJPuPY1fuDzWT1tp_xzfSNrh1B5LGUoUs7qc&dib_tag=se&keywords=LED%2Bbulb&qid=1714440786&s=industrial&sprefix=led%2Bbulb%2Cindustrial%2C450&sr=1-6&th=1), Quantity-01.
Connect the load in series with the Inverter.

Servo Motor:
Servo Motor1 (https://www.amazon.in/Robodo-Electronics-Tower-Micro-Servo/dp/B00MTFFAE0/ref=sr_1_1?crid=1JLSVAX2ZMLAE&dib=eyJ2IjoiMSJ9.vN0Ay0KXZUUvDpMlp9XZVveYBaxxAVEsW3hmKhU96wEv0nAqpMlQh-l-uAqNSjo2RccLdJeKxY5OKjuUpl8j-Ig68gDcuXWHGRB4diKMjprtOSFSYgEYHNyGFBQnSbfez3oLx66PRXj-gvdA121kC2jjbdJtLkSE9ZNYya7T5siHfnQ--DZlUYzmaMnpLLZkh_TcNuRsaLBrbgWQSK2VEQmkJMTW4M7GLs2qdL1EyhEB14HoWYKigFL7kY_eWiGy6DKkXO7pXMFRmOT3A5ZZJLquxDTstxeaYsLDeGv-vXU.q0S07q0qapR_xmsLC7_SaWTC4H6_fG0knm0jOT_kr7Y&dib_tag=se&keywords=servo+motor&qid=1714440997&refinements=p_89%3ARobodo&rnid=3837712031&s=industrial&sprefix=servo+%2Cindustrial%2C348&sr=1-1), Quantity- 01.
Glue it the solar pannel for the Tilt operation.
Servo Motor2 (https://www.amazon.in/gp/product/B0B7NVY1CC/ref=ox_sc_act_title_1?smid=A1K7XPNDUYG9CH&psc=1), Quantity-01.
Operation for the vertical motion. The MG90S servo motor has metal gear which helps to have more smooth operation under max.load.

Arduino Uno (https://www.amazon.in/Uno-Board-v3-04-Mini-Projects/dp/B0D1CBGQPQ/ref=sr_1_30?crid=22B7W7HP2FQH2&dib=eyJ2IjoiMSJ9.xBcfzO3hNvTg2yVn72TIi4CrGmDm8Ec_YHtmo4p6me4kPEKSbco27csKV8wgArW9WD0WU3X0p8p_EaVsUWKdJax1fuSx7d4mTdzRD5Eud_k.tSm0WfdIruffJMQbrY62CtaU3GKdbVb6ON2Yg1Vlm98&dib_tag=se&keywords=arduino+uno+generic&qid=1714441365&s=industrial&sprefix=arduino+uno+generic%2Cindustrial%2C384&sr=1-300), Quantity-01.
For the Tilt & vertical opertion. Controlling of Load through relay Module.

LDR sensor (https://www.amazon.in/MODULE-Optical-Photosensitive-Sensor-Arduino/dp/B07J45N5Z8/ref=sr_1_2_mod_primary_new?crid=2UC3OQ0U846DU&dib=eyJ2IjoiMSJ9.HUheqQuf-wUKitLOQbN5_jd52aXlLKVX9EuIAu3LQHx5Vtx-X8FkHnd_e_2K73r3qg-uWzsUPClzxBXIMpBXi5w23by5qPhiVsm0Twt68TXap0wc1fEwt1FFFpV7DCgsjPj0WIsGyNYG4h9TN4ccoU3qQD1DoP2_pd1vns3-6T4KS_eUJEgPV2Ps2JA2y-Eh1-3adxQlqGO9fuYm_0aYWnXqwD92Su5rL9PaBxZUf0qfCK4nzIB8Q4ZfXbbaLDOgXiXIVyzgl358PcoB_3DzqxbvpFOfbpEGnC8xUKUHOeU.k4ITX5Vu5Vx6NwWCtw3TGbQvCFLosWxlCbbldAHoLwY&dib_tag=se&keywords=generic+LDR+sensor&qid=1714441531&s=industrial&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=generic+ldr+sensor%2Cindustrial%2C345&sr=1-2), Quantity-04.
Here 2LDR for the Tilt operation & other 2LDR for the Vertical operation.

Relay Module (https://www.amazon.in/REES52-Channel-Relay-Module-Optocoupler/dp/B0CPT66LBP/ref=sr_1_16?crid=2OI4TZKMLLC5B&dib=eyJ2IjoiMSJ9.dPNYLQ8JzXc5cfHu3n2g4ELUpwlxxVWqnN1DQZSfp04bB8agkCBrw6V8Ic_GuAMnc_wKonpxyr2dR4T-Qz0Wxr2bjFAC7AZxJlap92l5Ok04DI8JM23eqW_NjOeCJpN96qGo2L3k0nDV6UyGiWUbrtxzNRoPMYOVB0OJr13JTxng5wI3_WCADmDqSkQJDrhaXURsbxg9VdEFzHI4InayHY70B_XrMVpF97GzAYrXLncnlEoE0fZ0nEE03BZzL6uBZlPmllGrrcPxrysgtywLe9i-U1cbJsfo1ImtDpOn7ag.TXKvG5q_rkkUbd0X5P-XGdomEkFpGoopisuRpdbXF5I&dib_tag=se&keywords=generic+12v+relay+module+with+optocoupler+with+diode&nsdOptOutParam=true&qid=1714441740&s=industrial&sprefix=generic+12v+relay+module+with+optocoupler+with+diode%2Cindustrial%2C318&sr=1-16), Quantity-01.
For the control of load through relay. Connect the Neutal of AC load to the COM pin & Line in series of load and Supply Line of Inverter at NO terminal.

Switch (https://www.amazon.in/Brass-Toggle-Rocker-Switch-Plastic/dp/B0B9JYGZYJ/ref=sr_1_22?crid=22PMUOXI5C5J&dib=eyJ2IjoiMSJ9.cDoQ-10gX1PfwwD9kHBnbXq_0RYrUjUXADqOW0xd3diL--K2zfzdMPyrd0bWLH_R7kAhXcf9abQQTB3GewbmdQRRAKZ9p1vZtxvWo2HJCt6iTF4pfs-sB8gTXULCSXnX2Paa26fvBl4w531CnNfBWxBaei88DoWmfne1umNolKjY6nhWyftv-wOebRKCEuByoln7wQzL4sKhuIWUMQZ1pKX8zU8oLmc16yhjuMVe9kUoRA7OucUGjrNsQN8xuhwo_4P8jfQcpW_SCBGreY3fBKlrUBJHfy85iB3v0uHno7Y.TTau0hgCiBWnSP7ss6pTmJ8OAUbOJSUmKd8MTvdrNdM&dib_tag=se&keywords=Switch+dc&qid=1714441966&s=industrial&sprefix=switch+dc%2Cindustrial%2C272&sr=1-22), Quantity-03.
Switch1: Between the Buck converter and the Cahrging module.
Switch2: Betwen the 7VDC supply and Arduino Uno.
Switch3: To control the relay.

That's it.
