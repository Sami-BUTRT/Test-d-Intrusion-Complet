# Test-d-Intrusion-Complet
Présentation du Projet
Ce projet réalisé dans le cadre de mon BUT Réseaux et Télécoms consiste en un audit complet de deux cibles vulnérables. L'objectif était d'identifier des failles critiques et de démontrer l'impact d'une exploitation réelle sur des systèmes obsolètes ou mal configurés.

Architecture du Laboratoire

Pour garantir la sécurité des tests, l'infrastructure a été déployée dans un environnement virtualisé totalement isolé du réseau physique.
Réseau : NAT Network (10.0.2.0/24) sous Oracle VirtualBox.
Attaquant : Kali Linux (10.0.2.10) avec Nessus Essentials et Metasploit.
Cible 1 : Windows XP Service Pack 1 (10.0.2.15).
Cible 2 : Metasploitable 2 (10.0.2.3).

Méthodologie

1. Analyse de Vulnérabilités (Nessus)
Utilisation de Nessus Essentials pour cartographier les vecteurs d'attaque.
Résultats critiques : Identification de 12 failles critiques sur Linux et 11 sur Windows.
Focus technique : Détection de la faille MS08-067 (SMB) et de la backdoor UnrealIRCd.

2. Exploitation (Metasploit & Meterpreter)
Démonstration de la prise de contrôle à distance pour valider la dangerosité des failles.
Sur Windows XP : Exploitation via NetAPI pour obtenir un shell Meterpreter avec les privilèges SYSTEM (le niveau le plus élevé).
Sur Metasploitable : Exploitation d'une porte dérobée permettant un accès root immédiat.

Préconisations de Sécurité
  L'audit conclut sur la nécessité vitale de :
  Migrer les systèmes obsolètes : Windows XP n'étant plus patché depuis 2014.
  Durcir les services : Désactivation des protocoles anciens comme SMBv1.
  Surveillance : Mise en place de scans de vulnérabilités réguliers.

Outils utilisés
  Hyperviseur : VirtualBox
  OS Attaque : Kali Linux
  Scanner : Nessus Essentials
  Framework : Metasploit (MSFConsole & Meterpreter)
