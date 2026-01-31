# Audit de Sécurité Offensif - Lab VirtualBox

## Présentation
Mise en place d'un environnement contrôlé pour simuler des attaques et tester des remédiations.

## Architecture du Lab
- **Attaquant :** Kali Linux (2024.x)
- **Cible 1 :** Metasploitable 2 (Linux vulnérable)
- **Cible 2 :** Windows XP SP2 (Non patché)
- **Réseau :** Host-only (Isolé d'Internet)

## Outils utilisés
- **Nmap :** Mapping réseau et détection de services.
- **Nessus :** Scan de vulnérabilités automatisé.
- **Metasploit Framework :** Exploitation des failles identifiées.

## POC (Proof of Concept)
1. Scan Nessus révélant la faille UnrealIRCd sur le port 6667.
2. Utilisation du module `exploit/unix/irc/unreal_ircd_3281_backdoor`.
3. Obtention d'un shell root sur la cible.
