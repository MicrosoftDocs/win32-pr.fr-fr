---
description: DirectShow Vue d’ensemble du système
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow Vue d’ensemble du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb7855277029adc563cc032740d3a59b3691fcf12ed2b2595d37a1abd0d923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966349"
---
# <a name="directshow-system-overview"></a>DirectShow Vue d’ensemble du système

**Le défi des médias**

L’utilisation de multimédia présente plusieurs défis majeurs :

-   Les flux multimédias contiennent de grandes quantités de données, qui doivent être traitées très rapidement.
-   L’audio et la vidéo doivent être synchronisés afin qu’ils démarrent et s’arrêtent en même temps et qu’ils soient lus à la même vitesse.
-   Les données peuvent provenir de nombreuses sources, y compris des fichiers locaux, des réseaux informatiques, des émissions de télévision et des caméras vidéo.
-   Les données sont disponibles dans différents formats, tels que Audio-Video entrelacé (AVI), le format ASF (Advanced Streaming Format), le MPEG (motion image experts Group) et la vidéo numérique (DV).
-   Le programmeur ne sait pas à l’avance quels périphériques matériels seront présents sur le système de l’utilisateur final.

**Solution DirectShow**

DirectShow est conçu pour résoudre chacun de ces problèmes. son principal objectif de conception est de simplifier la tâche de création d’applications multimédias numériques sur la plateforme Windows, en isolant les applications de la complexité des transports de données, des différences matérielles et de la synchronisation.

pour atteindre le débit nécessaire pour diffuser des données audio et vidéo, DirectShow utilise Direct3D et DirectSound chaque fois que cela est possible. Ces technologies affichent les données efficacement sur le son et les cartes graphiques de l’utilisateur. DirectShow synchronise la lecture en encapsulant les données multimédias dans des échantillons horodatés. pour gérer la diversité des sources, formats et périphériques matériels possibles, DirectShow utilise une architecture modulaire dans laquelle l’application combine et met en correspondance différents composants logiciels appelés *filtres*.

DirectShow fournit des filtres qui prennent en charge la capture et le paramétrage des appareils basés sur le Windows Driver Model (WDM), ainsi que des filtres qui prennent en charge les cartes de capture video for Windows (VfW) anciennes et les codecs écrits pour les interfaces ACM (Audio compression manager) et VCM (video compression manager).

le diagramme suivant illustre la relation entre une application, les composants DirectShow et certains composants matériels et logiciels pris en charge par DirectShow.

![architecture de haut niveau](images/arch-oview2.png)

comme illustré ici, DirectShow filtres communiquent avec, et contrôlent, un large éventail d’appareils, notamment le système de fichiers local, le tuner TV et les cartes de capture vidéo, les codecs VfW, l’affichage vidéo (par le biais de DirectDraw ou GDI) et la carte son (via DirectSound). ainsi, DirectShow isole l’application des nombreuses complexités de ces appareils. DirectShow fournit également des filtres de compression et de décompression natifs pour certains formats de fichiers.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de DirectShow](about-directshow.md)
</dt> </dl>

 

 



