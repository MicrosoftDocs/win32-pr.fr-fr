---
title: Espaces de couleurs dépendants de l’appareil
description: La plupart des espaces de couleurs sont dépendants des appareils.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Système de couleurs (WCS), espaces de couleurs dépendants du périphérique
- WCS (Windows color System), espaces de couleurs dépendants du périphérique
- gestion des couleurs des images, espaces colorimétriques dépendants du périphérique
- gestion des couleurs, espaces colorimétriques dépendants du périphérique
- couleurs, espaces de couleurs dépendants du périphérique
- espaces de couleurs, dépendant du périphérique
- espaces de couleurs dépendants du périphérique
- point blanc
- colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe10ad9d48e750f9869b113a45f1235d2aa692532702ea4443ec3629d32276ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593619"
---
# <a name="device-dependent-color-spaces"></a>Espaces de couleurs dépendants de l’appareil

La plupart des [espaces de couleurs](c.md) sont dépendants des appareils. Même si un appareil particulier, tel qu’une imprimante, peut utiliser l’espace colorimétrique CMJN, les couleurs qu’il affiche pour des valeurs CMJN spécifiques sont souvent légèrement différentes de celles des autres types d’imprimantes. C’est précisément pour cette raison que le système de gestion des couleurs WCS 1,0 est si utile.

Tous les espaces de couleurs ont un *point blanc*, qui est défini comme le blanc le plus blanc qui peut être produit dans cet espace colorimétrique. Étant donné que les appareils peuvent différer les uns des autres, leurs points blancs peuvent également différer. Toutes les couleurs qu’un appareil peut produire sont relatives à son point blanc. Par conséquent, un système de gestion des couleurs doit être en mesure de mapper le point blanc d’un espace de couleurs à un autre et de conserver les emplacements relatifs de toutes les couleurs. Il doit également être en mesure de mapper une couleur dans un espace de couleurs à sa correspondance la plus proche dans un autre espace colorimétrique, quelles que soient les différences entre les points blancs. WCS 1,0 peut effectuer ces deux tâches.

L’espace colorimétrique RVB est souvent utilisé sur les moniteurs d’ordinateurs. En tant que tel, il dépend de l’appareil. Les imprimantes utilisent généralement des [couleurs](c.md)CMJN. Chaque imprimante implémente sa propre version de l’espace colorimétrique CMJN. Les images numériques ne stockent pas réellement les couleurs. Ils peuvent stocker des numéros d’index dans une palette de couleurs. Le résultat est qu’il est très difficile pour les développeurs d’applications individuels d’utiliser ou de fournir une méthode standardisée pour déplacer des images de couleur d’un appareil vers un autre. Les professionnels de l’imagerie subissent généralement la frustration liée à la création d’une image graphique sur un écran d’ordinateur et à son fonctionnement très différent lors de son impression. WCS 1,0 répond à ces besoins en imagerie.

 

 




