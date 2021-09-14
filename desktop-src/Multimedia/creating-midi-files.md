---
title: Création de fichiers MIDI
description: Création de fichiers MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows multimédia, création de fichiers MIDI
- multimédia, création de fichiers MIDI
- audio multimédia, création de fichiers MIDI
- audio, création de fichiers MIDI
- Interface MIDI (Musical Instrument Digital Interface), création de fichiers
- MIDI (Musical Instrument Digital Interface), création de fichiers
- création de fichiers MIDI, à propos de
- L’Association de fabricants MIDI (MMA)
- MMA (Association de fabricants MIDI)
- Spécification détaillée MIDI
- Spécification des fichiers MIDI standard
- Spécification générale MIDI (GM)
- Spécification GM (General MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011771"
---
# <a name="creating-midi-files"></a>Création de fichiers MIDI

Les spécifications MIDI (Musical Instrument Digital Interface) sont publiées par et sont des documents protégés par des droits d’auteur de l’Association de fabricants MIDI (MMA). La liste suivante décrit les spécifications qui présentent le plus grand intérêt général :

## <a name="midi-detailed-specification"></a>Spécification détaillée MIDI

La spécification détaillée MIDI explique les protocoles matériels et logiciels MIDI. Cela est utile pour les applications de développement multimédia qui implémentent la prise en charge MIDI en utilisant des fonctions MIDI pour enregistrer, modifier et/ou lire des données MIDI.

## <a name="standard-midi-files-10"></a>Fichiers MIDI standard 1,0

La spécification de fichiers MIDI standard définit un moyen d’échanger des données MIDI horodatées entre différentes applications sur des plateformes matérielles identiques ou différentes. Cela est utile pour les développeurs qui écrivent des applications qui lisent et analysent les fichiers de disque contenant des données MIDI et/ou écrivent des fichiers de données MIDI sur le disque.

## <a name="general-midi-system---level-1"></a>Système MIDI général-niveau 1

La spécification standard MIDI (GM) définit une configuration MIDI minimale d’un « système MIDI général ». Ce système se compose d’une classe spécifique de périphériques de lecture MIDI et présente un intérêt pour les développeurs multimédias qui créent des fichiers MIDI. La plupart des cartes son et des synthétiseurs MIDI fabriqués aujourd’hui sont compatibles avec la spécification GM. Les fichiers MIDI qui sont créés dans la spécification GM doivent généralement sembler tels qu’ils étaient prévus, quel que soit l’appareil compatible GM sur lequel ils sont lus.

pour permettre aux fichiers midi d’être un format viable pour représenter de la musique dans le calcul multimédia, Windows suit la spécification General MIDI System Level 1. Les rubriques suivantes fournissent des instructions de création MIDI supplémentaires :

-   [Instructions de création pour les fichiers MIDI](authoring-guidelines-for-midi-files.md)
-   [Attributions de correctifs MIDI standard](standard-midi-patch-assignments.md)
-   [Attributions de clés MIDI standard](standard-midi-key-assignments.md)

 

 




