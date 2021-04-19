---
title: Espaces de couleurs indépendants de l’appareil
description: Reconnaissant la nécessité de mesures de couleur standard, indépendantes des appareils, la Commission internationale de l’Eclairage (Commission internationale sur l’éclairage) ou CIE, a créé un espace de couleurs basé sur \ 0034 ; imaginaire-0034 ; couleurs principales.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Système de couleurs Windows (WCS), espaces de couleurs indépendants du périphérique
- WCS (système de couleurs Windows), espaces de couleurs indépendants du périphérique
- gestion des couleurs des images, espaces de couleurs indépendants du périphérique
- gestion des couleurs, espaces de couleurs indépendants du périphérique
- couleurs, espaces de couleurs indépendants du périphérique
- espaces de couleurs, indépendants du périphérique
- espaces de couleurs indépendants du périphérique
- Commission internationale de l’Eclairage (CIE)
- International Commission on illumination (CIE)
- CIE (Commission international de l’Eclairage)
- CIE (Commission internationale sur l’éclairage)
- Espace de couleurs CIEXYZ
- Espace de couleurs XYZ
- espace colorimétrique sRVB
- espaces de couleurs, CIEXYZ
- espaces de couleurs, sRVB
- espaces de couleurs, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/26/2021
ms.locfileid: "106539363"
---
# <a name="device-independent-color-spaces"></a>Espaces de couleurs indépendants de l’appareil

Reconnaissant la nécessité de mesures de couleur standard, indépendantes des appareils, la Commission internationale de l’Eclairage (Commission internationale sur l’éclairage) ou CIE, a créé un [espace de couleurs](c.md) basé sur les [couleurs primaires](p.md)« imaginaires ». Aucun appareil réel ne devrait produire des couleurs dans cet espace colorimétrique. Il est utilisé comme moyen de convertir les couleurs d’un espace de couleurs à un autre. Les couleurs primaires de cet espace colorimétrique sont les couleurs abstraites X, Y et Z.

L’espace de couleurs 1931 CIEXYZ est largement utilisé comme base pour la conversion de l’espace colorimétrique. Avec l’avènement d’Internet, toutefois, les considérations relatives à la bande passante ont rendu l’espace de couleurs XYZ plus complexe. L’échange d’images sur la bande passante limitée d’Internet nécessite un modèle de [couleurs](c.md)plus compact.

Par conséquent, Hewlett-Packard et Microsoft ont proposé l’adoption d’un espace de couleurs RVB prédéfini standard, connu sous le nom d’sRGB, afin de permettre une gestion des couleurs précise avec très peu de surcharge de données. Cette norme a été approuvée comme norme internationale officielle par le Commission Électrotechnique Internationale (IEC) en tant que IEC 61966-2-1 : systèmes multimédias et mesure EquipmentColour et ManagementPart 2-1 : Color ManagementDefault RGB Color Space. Elle est disponible directement à partir du service IEC à l’adresse <https://www.iec.ch/> . Les informations qui décrivent les problèmes techniques inhérents à sRVB sont disponibles sur Internet à l’adresse suivante :

[Un espace de couleurs par défaut standard pour Internet-sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

Une version de fichier d’aide d’un livre blanc traitant des problèmes techniques liés à sRVB, sRVB. HLP, est disponible dans le \\ dossier d’aide du Guide de référence du programmeur WCS 1,0 dans le kit de développement logiciel (SDK) de la plateforme.

Différents formats de fichiers peuvent utiliser ou ajouter un indicateur pour spécifier que l’image se trouve dans l’espace de couleurs sRVB. Dans le format DIB (Device-Independent Bitmap) Windows, la définition du membre **bV5CSType** de la structure [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) sur LCS \_ sRVB spécifie que les couleurs DIB se trouvent dans l’espace de couleurs sRVB.

 

 




