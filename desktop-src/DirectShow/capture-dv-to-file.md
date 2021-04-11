---
description: Capturer le fichier DV dans un fichier
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturer le fichier DV dans un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317742"
---
# <a name="capture-dv-to-file"></a>Capturer le fichier DV dans un fichier

Cette section décrit comment capturer une vidéo numérique (DV) à partir d’une caméra DV ou d’une bande VTR.

1.  Créez une instance du filtre de [pilote MSDV](msdv-driver.md) . Pour plus d’informations, consultez [sélection d’un périphérique de capture](selecting-a-capture-device.md).
2.  Initialisez le générateur de graphiques de capture, comme décrit dans [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).
3.  Générez le graphique de capture, en fonction du type de fichier cible :
    -   [Capturer un fichier DV de type 1](capture-a-type-1-dv-file.md)
    -   [Capturer un fichier DV de type 2](capture-a-type-2-dv-file.md)
    -   [Capturer le DV avec la couleur RVB non compressée](capture-dv-to-uncompressed-rgb.md)
4.  Exécutez le graphique.

La capture à partir d’une bande VTR fonctionne comme la capture de vidéos en direct à partir de l’appareil photo, sauf que vous devez lire la bande, comme décrit dans [contrôle d’un caméscope DV](controlling-a-dv-camcorder.md). Pour éviter de perdre des frames, exécutez d’abord le graphique, puis jouez la bande. Lorsque vous avez terminé la transmission, arrêtez d’abord la bande, puis arrêtez le graphique.

> [!Note]  
> Le caméscope doit être en mode VTR. Consultez [mode](device-mode.md)de l’appareil.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Types-1 et fichiers AVI DV type-2](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 



