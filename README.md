# HARD
# !/usr/bin/python
# -*- coding: utf-8 -*-
import os
from scapy.all import *
DoS=0.0
MiM=0.0
Ramsomware=0.0
Adware= 0.0
Usuario = 0.85
si = True
no = False
CU=0
def Menu():
     """

     Función que limpia la pantalla y muestra nuevamente el menu

     """

     os.system('cls')  # NOTA para windows tienes que cambiar clear por cls

     print("Selecciona una opción")

     print("\t1 - Cuestionario tecnico")

     print("\t2 - Cuestionario Usuario")

     print("\t3 -  Resultado")

     print("\t4 -  Prueba")

     print("\t9 - salir")


while True:

     # Mostramos el menu

     Menu()

     # solicituamos una opción al usuario

     opcionMenu = input("inserta un numero valor >> ")
     if opcionMenu == "1":
         # Valor por pais
         Mex = 0.1201
         # Empresa
         AdWare = 0.083
         Ramsomware = 0.0
         MiM = 0.0
         DoS = 0.0


         p1 = eval(input('¿Los usuarios tienen permisos privilegiados y pueden descargar de Internet? '))
         if p1 == True:
             AdWare = AdWare
             MiM = MiM + 0.03
             DoS = DoS + 0.08
         #   print(AdWare)
         p2 = eval(input('¿Se cuenta con sistema Antivirus? '))
         if p2 == True:
             AdWare = AdWare - 0.2
             Ramsomware = Ramsomware - 0.15
             MiM = MiM - 0.09
             DoS = DoS - 0.04
             p2_1 = eval(input('¿El antivirus tiene habilitado el bloqueo de ventanas emergentes? '))
             if p2_1 == True:
                 AdWare = AdWare - 0.23
                 Ramsomware = (Ramsomware * AdWare) / Ramsomware
                 # print(Ramsomware)
             elif p2_1 == False:
                 AdWare = (AdWare * 0.8) / (AdWare * 0.8) + (0.2 * 0.23)
                 #print(AdWare)

                 Ramsomware = (Ramsomware * AdWare) / Ramsomware
                 # print(Ramsomware)
         elif p2 == False:
             Ramsomware = Ramsomware + 0.35
             MiM = MiM + 0.07
             DoS = DoS + 0.06
             AdWare = AdWare + 0.421
         # print(AdWare)
         p3 = eval(input("¿Se cuenta con Firewall?"))
         if p3 == True:
             DoS = DoS - 0.37
             p3_1 = eval(input("¿El Firewall filtra el direccionamiento?"))
             if p3_1 == True:
                 Dos = (DoS * 0.41) / (DoS * 0.41) + (0.63 * 0.59)

             elif p3_1 == False:
                 DoS = (0.63 * 0.59) / (DoS * 0.41) + (0.63 * 0.59)

         p5 = eval(input("¿El SITE cuenta con sistema de vigilancia?"))
         if p5 == True:
             DoS = (DoS - 0.13)
             MiM = MiM - 0.21

         p6 = eval(input("Se tienen sensore PRTG"))
         if p6 == True:
             DoS = (DoS - 0.35)
         elif p6 == False:
             DoS = DoS + 0.15

         p7 = eval(input( "El sistema operativo que utilizan los equipos de los usuarios es: \n 1)Windows \t 2)Distribucion de Linux \t 3)OS X(Distribucion de Apple"))

         if p7 == 1:
             AdWare = AdWare + 0.36
         elif p7 == 2:
             Adware = AdWare + 0.01
         elif p7 == 3:
             AdWare = AdWare + 0.02
         CU = eval(input("¿Cuantos usuarios se tienen?"))
         if CU > 0:
             CU = CU * 0.1



         input("\npulsa una tecla para continuar")

     elif opcionMenu == "2":
         input("color favorito")
         input("Usas paraguas cuando llueve?")
         T1 = eval(input("Si recibe un mensaje de texto de su entidad bancaria anunciándole que acaba de ganarse un premio, usted: \n 1)Se comunica con su institucion bancaria \t 2)Se apresura para resivir su premio"))
         if T1 == 1:
             Usuario = Usuario + 0.13
         elif T1 == 2:
             Usuario = Usuario - 0.26

         input("¿Usas constantemente redes sociales?")
         T2 = eval(input("¿Confias en las buenas intenciones de las personas?"))
         if T2 == True:
             Usuario = Usuario - 0.17
         elif T2 == False:
             Usuario = Usuario + 0.04
         T4 = eval(input("En caso de que en su cuenta de ahorros aparezca un dinero con el que no contaba, usted lo cobraria?  "))
         if T4 == True:
             Usuario = Usuario - 0.26
         elif T4 == False:
             Usuario = Usuario + 0.11
         T5 = eval(input("Cuál es la manera más frecuente a través de la cual accede al portal de su entidad bancaria \n 1)Mediante red publica (WIFI publico) \t 2)Mediante Red privada (Red casa o trabajo)?"))
         if T5 == 1:
             T6 = eval(input("¿En que dispositivo \n 1)Mediante computadora \t 2)Mediante aplicacion?"))
             if T6 == 1:
                 Usuario = Usuario - 0.21
             elif T6 == 2:
                 Usuario = Usuario - 0.43
         if T5 == 2:
             T6 = eval(input("¿En que dispositivo \n 1)Mediante computadora \t 2)Mediante aplicacion?"))
             if T6 == 1:
                 Usuario = Usuario - 0.137
             elif T6 == 2:
                 Usuario = Usuario - 0.161

         print("")
         input("\npulsa una tecla para continuar")

     elif opcionMenu == "3":
         acomodo = [Ramsomware, MiM, DoS, AdWare]
         mayor = acomodo[0]
         for acomodo in acomodo:
             if acomodo > mayor :
                 mayor = acomodo
                 print(mayor)


         Ramsomware = Ramsomware + CU
         if Ramsomware >1:
             print("Se teienen alatas probabilidades de un ataque Ramsomware")
             print("Se necesita tener cuidado con sistemas Adware ya que representan un riesgo por la baja fiabilidad de sus usuarios")
             print("Se recomienda no alamacenar informacion de forma local en los equipos de computo y en casa de ya tenerse almacenada\nmandar a un servidor")
             print("Se debe dara capacitacion a los usuarios respecto a en que consiste la ingenieria social y como actuar para evitar caer en sus tacticas ")
         elif MiM > 1:
             print("")



         print("")

         input("\npulsa una tecla para continuar")

     elif opcionMenu == "4":
         b = sniff(count=30)
         b.nsummary()
         

         print("*******************************No se logro realizar un envenenamiento por ARP************************************************")

     elif opcionMenu == "9":

          break

     else:

          print("")

          input("No has pulsado ninguna opción correcta...\npulsa una tecla para continuar")

while True:
     Menu()
