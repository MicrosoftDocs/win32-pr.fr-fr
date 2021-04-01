---
description: Classifications bitmap
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Classifications bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202058"
---
# <a name="bitmap-classifications"></a>Classifications bitmap

Il existe deux classes de bitmaps :

-   [Bitmaps indépendantes du périphérique](device-independent-bitmaps.md) (DIB). Le format de fichier DIB a été conçu pour garantir que les graphiques bitmap créés à l’aide d’une application peuvent être chargés et affichés dans une autre application, conservant ainsi la même apparence que l’original.

-   Les [bitmaps dépendantes](device-dependent-bitmaps.md) de l’appareil (DDB), également appelées bitmaps GDI, étaient les seules bitmaps disponibles dans les versions antérieures de Microsoft Windows 16 bits (antérieures à la version 3,0). Toutefois, à mesure que la technologie d’affichage a été améliorée et que la diversité des périphériques d’affichage disponibles a augmenté, certains problèmes inhérents, qui ne pouvaient être résolus qu’à l’aide de DIB, sont certains problèmes. Par exemple, il n’existait aucune méthode de stockage (ou d’extraction) de la résolution du type d’affichage sur lequel une image bitmap a été créée, de sorte qu’une application de dessin n’a pas pu déterminer rapidement si une image bitmap était adaptée au type de périphérique d’affichage vidéo sur lequel l’application s’exécutait.

    Malgré ces problèmes, DDB (également connu sous le nom de bitmaps compatibles) est toujours utile pour de meilleures performances GDI et dans d’autres situations.

 

 



