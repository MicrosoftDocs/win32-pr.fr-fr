---
description: Instructions générales pour l’implémentation de codecs BRUTs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Instructions générales pour l’implémentation de codecs BRUTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226164"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a>Instructions générales pour l’implémentation de codecs BRUTs

Par rapport aux types d’images non BRUTes, tels que JPEG ou TIFF, il existe deux différences notables dans la façon dont les formats d’images BRUTes sont censés se comporter dans Windows :

-   La plupart des formats d’images BRUTs sont supposés être « en lecture seule » et ne prendront probablement pas en charge l’encodage de pixel au format brut. toutefois, étant donné que Windows composant d’imagerie (WIC) requiert un encodeur pour prendre en charge les métadonnées en écriture différée, les auteurs de codec brut doivent envisager d’implémenter au moins une classe de codeur squelette.
-   Le décodage d’une image brute de taille réelle peut prendre beaucoup de temps par rapport à d’autres formats. Pour cette raison, Microsoft recommande de prendre certaines approches pour réduire la latence du décodage et garantir la prise en charge des scénarios tels que le rendu rapide des miniatures et des préversions.

    Par exemple, tous les auteurs de codec brut doivent implémenter l’interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , qui fournit un mécanisme pour notifier le décodeur à l’avance de la taille de la bitmap cible, ce qui permet d’optimiser le décodage vers une plus petite taille d’image de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



