##### Allgemeine Info:

Das Hauptprogramm besteht aus einem großen Simulink-Block, in welchem die Teilsysteme als einzelne State-Blocke mit UND-Verknüpfung implementiert sind. Für die Simulation sind die schon in Simulink gegebene Signal und Routing Blocks verwendet.

##### Namem:

@ Taster:

DK_seite: Der Taster an der Seite der Drehplattform. Wird verwendet zum Stoppe der rotierende Bewegung der Plattform, wenn sie die richtige Stelle erreicht.

PK_oben: Der Taster an der Turmvorrichtung, der ganz oben an der Ende der Führung steht. Dieser Taster dient zum Stoppen der translatorischen Bewegung der Turmvorrichtung nach oben, wenn der Ende erreicht ist.

SK: Der Taster hinter der Stab, der die Würfel nicht auszufallen hält. Zeigt, wenn der Stab herausnehmen ist. (Es kann sein, dass dieser Taster in spätere Implementationen nicht mehr verwendet wird).

@ Signale (Input):

encoder: Das Signal des Encoders des Motors an dem Förderbahn. Wird benutzt zum Erkennen von Verklemmungen des Förderbahns. 

sensor: Die Lichtschranke, die erkennt, wenn ein Würfel zur Eingabe in der Turmvorrichtung vorhanden ist.

@ Signale (Output):

verklemmung: Zeigt wenn eine Verklemmung an dem Förderbahn passiert (nur zum Debbugen und interne Sachen verwendet)

led: Die Zustand-LED, die leuchtet wenn das Programm fertig ist

Gruppe der Motoren:
  
  *MOTOR_INITIALEN*_pwm: PWM des Motors geben in Prozent
 
  *MOTOR_INITIALEN*_richtung: Richtung des Motors (am meistens 0 nach vorne, 1 nach hinten, aber hängt von   dem Verwendung ab. In dem Statefow Block ist es    besser erklärt)

  MOTOR_INITIALEN:

	+DM: Der Motor für die rotierende Bewegung der Turmvorrichtung 

	+FM: Der Motor für die Steuerung des Förderbahns

	+PM: Der Motor für die Steuerung der Ladeplattform des Turmovrrichtung

	+SM: Der Motor für die Steuerung des Turmschiebers

	+TM1, TM2: Die Motoren für die translatorische Bewegung der Turmvorrichtung

	+STM: Der Motor für die Bewegung des Stabs an der Turmvorrichtung

#### Funktionsweise

*wird geben*
