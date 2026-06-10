#LAB 23 - JNI Protection (Anti-Debug) - Native
Projet Android Java + C++ (NDK) qui illustre comment structurer un module JNI defensif:

expose une API JNI claire (booleens + rapport texte)
journalise cote natif (Logcat)
adapte l'interface Android selon l'etat detecte
Note importante (TP defensif)
Ce TP est educatif. Il montre comment detecter des conditions anormales de maniere raisonnable, mais ne cherche pas a fournir des techniques d'evasion avancees.

Prerequis
Android Studio
NDK + CMake installes (SDK Manager)
Lancer
Ouvrir le dossier dans Android Studio, Sync, Run.

API JNI
NativeDefense.isDebuggerDetected(context) -> boolean
NativeDefense.getSecurityReport(context) -> String
Le code Java complete les checks "safe" (debuggable build, debugger connecte). Le natif sert a:

centraliser l'etat
logger cote natif
remonter un rapport
