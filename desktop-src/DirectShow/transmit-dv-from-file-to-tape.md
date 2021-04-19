---
description: Transmettre le fichier DV du fichier à la bande
ms.assetid: f6dd8c4b-0535-42b9-a969-89e7b9e6ee0f
title: Transmettre le fichier DV du fichier à la bande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415a12f0876d3bd8e2a46de58b15f96f3eba3e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529366"
---
# <a name="transmit-dv-from-file-to-tape"></a>Transmettre le fichier DV du fichier à la bande

La transmission d’un fichier DV AVI à VTR Tape est compliquée par le fait que les fichiers peuvent être de type-1 ou-2. Pour transmettre un fichier DV à une bande, procédez comme suit :

1.  Créez une instance du filtre de [pilote MSDV](msdv-driver.md) . Pour plus d’informations, consultez [sélection d’un périphérique de capture](selecting-a-capture-device.md).
2.  Assurez-vous que l’appareil est en mode VTR. Dans le cas contraire, vous ne pourrez pas transmettre à la bande. Consultez [mode](device-mode.md)de l’appareil.
3.  Initialisez le générateur de graphiques de capture, comme décrit dans [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).
4.  Générez le graphique. La configuration du graphique dépend du type de fichier DV :
    -   [Transmettre à partir d’un fichier de type-1](transmit-from-type-1-file.md)
    -   [Transmettre à partir du fichier de type 2](transmit-from-type-2-file.md)
5.  Mettez l’appareil en mode de pause d’enregistrement, comme décrit dans [contrôle d’un caméscope DV](controlling-a-dv-camcorder.md).
6.  Suspendez le graphique de filtre. Lorsque le graphique de filtre est suspendu, il envoie un flux continu qui répète la première image de la vidéo.
7.  Pour commencer la transmission, mettez l’appareil en mode enregistrement, puis exécutez le graphique de filtre. L’appareil prend un certain temps jusqu’à ce que la tête d’enregistrement puisse enregistrer, donc patientez environ deux secondes avant d’exécuter le graphique. Cela peut entraîner quelques images dupliquées au début de la bande, mais elle garantit qu’aucune donnée n’est perdue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique dans DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



