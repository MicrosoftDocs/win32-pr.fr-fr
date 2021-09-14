---
title: configuration de Flux vidéo pour la recherche de performances
description: configuration de Flux vidéo pour la recherche de performances
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flux, configuration de flux vidéo
- codecs, configuration des flux vidéo
- flux vidéo, configuration
- flux vidéo, performances
- performances, flux vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219572"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>configuration de Flux vidéo pour la recherche de performances

Certaines applications de lecture effectuent beaucoup de recherches sur des flux individuels. La recherche est une zone où les performances peuvent varier considérablement en fonction des paramètres du flux. Si vous savez que votre contenu doit être optimisé pour une recherche rapide, vous pouvez adapter la configuration de votre flux pour améliorer les performances.

Le plus grand facteur affectant la vitesse des opérations de recherche dans la vidéo est l’espacement des images clés. Étant donné que chaque trame entre les images clés doit être reconstruite en fonction des frames qui le précèdent, les images clés largement espacées génèrent des temps de recherche plus longs. Par exemple, si un flux vidéo de 30 images par seconde a un espacement de trame de clé maximal de 10 secondes, il y a potentiellement 300 images entre les images clés. Si vous recherchez la dernière [*image Delta*](wmformat-glossary.md), 299 frames doivent être reconstruits pour que le frame soit décompressé. Si chaque reconstruction de frame a pris 0,01 seconde, la recherche prendrait presque 3 secondes. Si vous souhaitez augmenter l’efficacité de la recherche, il peut être utile de réduire l’espacement entre les images clés. Toutefois, si vous définissez les images clés trop près, vous risquez de perdre la qualité.

Vous pouvez définir l’espacement maximal de l’image clé en appelant [**IWMVideoMediaProps :: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing). Les valeurs recommandées, basées sur la vitesse de transmission du flux, sont répertoriées dans le tableau suivant. Ces valeurs fournissent un bon compromis entre les performances et la qualité. Le kit de développement logiciel (SDK) n’impose aucune limite de temps entre les images clés. En général, les temps de plus de 30 secondes peuvent nuire aux heures de recherche lorsque le contenu est diffusé sur un réseau et lorsqu’il est lu localement.



| Vitesse de transmission             | Espace d’image clé maximal suggéré |
|----------------------|-------------------------------------|
| de 22 Kbits/s à 300 Kbits/s  | 8 secondes                           |
| 300 Kbits/s à 600 kbps | 6 secondes                           |
| 600 Kbits/s à 2 Mbits/s   | 4 secondes                           |
| 2 Mbits/s et plus    | 3 secondes                           |



 

Pour plus d’informations sur l’obtention des meilleures performances lors de la recherche de fichiers vidéo, consultez [obtention de meilleures performances de recherche de vidéos](getting-the-best-video-seeking-performance.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> </dl>

 

 




