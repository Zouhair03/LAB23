LAB 23 – Protection JNI : Détection de Débogage (Anti-Debugging)

Ce projet Android, développé en Java et C++ à l’aide du NDK, présente la mise en place d’un module JNI destiné à renforcer la sécurité de l’application face aux tentatives de débogage.

Objectifs

* Concevoir une interface JNI simple et cohérente basée sur des retours booléens et des rapports textuels.
* Enregistrer les événements de sécurité côté natif via Logcat.
* Adapter dynamiquement le comportement de l’interface Android en fonction des anomalies détectées.

Contexte pédagogique

Ce laboratoire a une vocation exclusivement éducative. Son objectif est de démontrer comment identifier certaines situations potentiellement suspectes de manière raisonnable et transparente, sans recourir à des mécanismes avancés d’évasion ou de contournement.

Prérequis

* Android Studio installé.
* Android NDK et CMake configurés depuis le SDK Manager.

Exécution du projet

1. Ouvrir le projet dans Android Studio.
2. Effectuer la synchronisation des dépendances.
3. Compiler et lancer l’application sur un appareil ou un émulateur.

Interface JNI exposée

* NativeDefense.isDebuggerDetected(context) → retourne un booléen indiquant la présence éventuelle d’un débogueur.
* NativeDefense.getSecurityReport(context) → génère un rapport textuel détaillant l’état de sécurité observé.

Répartition des responsabilités

Les vérifications de base, telles que la détection d’un build débogable ou d’un débogueur connecté, sont réalisées côté Java. Le composant natif a pour rôle de :

* centraliser les informations liées à la sécurité ;
* produire des journaux d’événements dans Logcat ;
* fournir un rapport synthétique exploitable par l’application.