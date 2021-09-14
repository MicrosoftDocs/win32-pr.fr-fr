---
description: Comment un flux vidéo encodé à l’aide de la méthode VBR basée sur la qualité a-t-il moins de frames que le flux d’origine ?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Comment un flux vidéo encodé à l’aide de la méthode VBR basée sur la qualité a-t-il moins de frames que le flux d’origine ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127415835"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>Comment un flux vidéo encodé à l’aide de la méthode VBR basée sur la qualité a-t-il moins de frames que le flux d’origine ?

Le nombre de frames d’un flux encodé peut être inférieur au nombre de frames de l’original pour l’une des deux raisons suivantes : les images dupliquées et les frames déplacés.

En règle générale, l’encodeur ne produit pas de frames qui sont des doublons exacts du frame précédent. Si vous avez besoin d’un échantillon pour chaque frame (requis par certains conteneurs, par exemple), vous pouvez configurer l’encodeur pour produire des frames « factices » en affectant à la propriété [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) la \_ valeur variant true.

L’encodeur supprime les frames lorsqu’il ne peut pas encoder tous les frames sans débordement de la mémoire tampon. Les frames supprimés ont une incidence sur la qualité du flux, ce qui n’est pas le cas des trames dupliquées.

Vous pouvez obtenir des statistiques de frame à partir de l’encodeur pour déterminer si des frames ont été supprimés. Pour plus d’informations, consultez [obtention de statistiques de codage](gettingencodingstatistics.md).

En règle générale, les flux VBR basés sur la qualité n’auront que moins de frames que l’original s’il y a des images en double (car la vitesse de transmission n’est pas restreinte).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Questions fréquentes (FAQ)](frequentlyaskedquestions.md)
</dt> </dl>

 

 



