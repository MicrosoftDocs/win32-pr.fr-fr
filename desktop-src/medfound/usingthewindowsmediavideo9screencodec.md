---
description: Utilisation du codec d’écran Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Utilisation du codec d’écran Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538038"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a>Utilisation du codec d’écran Windows Media Video 9 (Microsoft Media Foundation)

Le codec d’écran Windows Media Video 9 est optimisé pour la compression de la vidéo de l' *application*, qui se compose de captures d’écran consécutives pour un affichage d’ordinateur. Le codec tire parti de la simplicité d’image classique (relativement peu de couleurs, beaucoup de lignes droites, etc.) et du manque de mouvement relatif pour obtenir un taux de compression très élevé. L’inconvénient de cette optimisation est que la vidéo qui n’est pas conforme aux caractéristiques attendues de la vidéo d’application peut être difficile à compresser avec un niveau de qualité acceptable.

L’encodeur d’écran Windows Media Video 9 est identifié par l’identificateur de classe CLSID \_ CMSSEncMediaObject2 et le décodeur est identifié par l’identificateur de classe CLSID \_ CMSSDecMediaObject. La valeur FOURCC pour les types de média utilisant ce codec est « MSS2 ».

## <a name="configuring-the-encoder"></a>Configuration de l’encodeur

L’encodeur du codec d’écran Windows Media Video 9 est configuré de la même façon que le décodeur vidéo standard.

> [!Note]  
> L’encodeur d’écran ne prend en charge qu’un seul encodage à passage. Vous pouvez définir la propriété [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) sur 2 et traiter les entrées deux fois sans erreur, mais il n’y a aucun avantage à le faire. Il s’agit d’un problème connu qui peut être corrigé dans les versions ultérieures.

 

## <a name="getting-the-best-results"></a>Obtention des meilleurs résultats

Si vous découvrez que la qualité souhaitée dans le contenu de la capture d’écran nécessite une vitesse de transmission supérieure à celle que vous pouvez utiliser pour votre scénario de distribution, vous pouvez essayer les techniques suivantes pour obtenir plus d’efficacité à partir du codec :

-   Utilisez une résolution plus petite pour la capture d’écran. La capture d’une résolution d’écran plus grande que nécessaire peut confondre la visionneuse en présentant des informations inutiles.
-   Utilisez une fréquence d’images plus lente. Les captures d’écran peuvent souvent être efficaces à des fréquences d’images très basses (parfois jusqu’à 4 ou 5 images par seconde).
-   Utilisez moins de graphiques dans la capture d’écran. Le codec d’écran Windows Media Video 9 est optimisé pour encoder des primitives Windows et du texte de haute qualité. En général, des problèmes se produisent en raison des graphiques bitmap, qui contiennent souvent des milliers de couleurs individuelles. Moins il y a d’images bitmap à l’écran lors de la capture, plus vos résultats seront nombreux. Si vous ne pouvez pas éliminer les graphiques de la capture d’écran, il existe plusieurs façons de réduire l’impact d’une image bitmap sur la qualité de l’image :
    -   Réduisez la taille du graphique.
    -   Réduisez le nombre de graphiques individuels qui s’affichent à l’écran en même temps.
    -   Réduisez la quantité de mouvement du graphique. Par exemple, si le graphique est dans une fenêtre, laissez la fenêtre aussi stationnaire que possible.
    -   Évitez de déplacer le pointeur de la souris sur le graphique, ou de faire glisser des fenêtres ou d’autres éléments sur le graphique.

## <a name="decoding"></a>Décodage

Il n’existe aucune exigence particulière pour décoder la vidéo de capture d’écran. Toutefois, comme pour tous les codecs Windows Media Video 9, le décodeur de capture d’écran ne peut pas décompresser correctement le contenu encodé sans les données privées du codec.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’encodage vidéo](configuringvideoencoding.md)
</dt> <dt>

[Utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md)
</dt> <dt>

[Encodeur d’écran Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 



