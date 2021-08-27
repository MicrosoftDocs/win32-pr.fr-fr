---
title: obtenir de bons résultats avec le Codec d’écran Windows Media Video 9
description: obtenir de bons résultats avec le Codec d’écran Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Windows Media Format SDK, Windows Media Video 9 codec d’écran
- ASF (Advanced Systems Format), Windows Media Video 9 codec d’écran
- ASF (Format des systèmes avancés), Windows Media Video 9 codec d’écran
- codecs, Windows Media Video 9 écran
- Windows Codec vidéo sur Media 9, résultats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657cde745f6bfbabe00fe123b493e2eae2afb20ddf40206f781822770a4386f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110429"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a>obtenir de bons résultats avec le Codec d’écran Windows Media Video 9

le codec d’écran Windows Media Video 9 est conçu pour produire des vidéos hautement compressées pour la capture d’écran. Étant donné que la plupart des besoins en matière de capture d’écran impliquent des images statiques et simples, les niveaux élevés de compression atteints ne signifient généralement pas un véritable sacrifice de la qualité de l’image. Toutefois, chaque capture d’écran est différente, et la qualité d’image résultante peut varier considérablement selon les circonstances.

La meilleure façon de déterminer les paramètres de profil pour une session de codec d’écran consiste à encoder un fichier de test à l’aide d’un flux de vitesse de transmission variable basé sur la qualité. Définissez la qualité sur la valeur souhaitée et encodez une capture d’écran comme si vous enregistriez le fichier final. Lorsque le fichier est écrit, lisez-le à l’aide de l’objet lecteur asynchrone, en effectuant des appels réguliers à [**IWMReaderAdvanced :: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics). En surveillant la valeur du membre **dwBandwidth** de la structure [**des \_ \_ statistiques du lecteur WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) pour chaque appel, vous pouvez déterminer la vitesse de transmission approximative requise pour obtenir la qualité souhaitée. Vous pouvez ensuite utiliser ce taux de bits pour l’encodage à débit binaire constant.

Si vous découvrez que la qualité que vous souhaitez nécessite une vitesse de transmission supérieure à celle que vous pouvez utiliser pour votre scénario de distribution, vous pouvez essayer les techniques suivantes pour obtenir plus d’efficacité à partir du codec.

-   Utilisez une résolution plus petite pour la capture d’écran. La capture d’une résolution d’écran supérieure à celle dont vous avez besoin peut également créer une confusion pour la visionneuse en présentant plus d’informations que nécessaire.
-   Utilisez moins de graphiques dans la capture d’écran. le codec d’écran Windows Media Video 9 est optimisé pour encoder des primitives Windows et du texte de haute qualité. En général, des problèmes se produisent en raison des graphiques bitmap, qui contiennent souvent des milliers de couleurs individuelles. Moins il y a d’images bitmap à l’écran lors de la capture, plus vos résultats seront nombreux. Si vous ne pouvez pas éliminer les graphiques de la capture d’écran, il existe plusieurs façons de réduire l’impact d’une image bitmap sur la qualité de l’image :
    -   Réduisez la taille du graphique.
    -   Réduisez le nombre de graphiques individuels qui s’affichent simultanément sur l’écran.
    -   Réduisez la quantité de mouvement du graphique. Par exemple, si le graphique est dans une fenêtre, laissez la fenêtre aussi stationnaire que possible.
    -   Évitez de déplacer le pointeur de la souris sur le graphique, ou de faire glisser des fenêtres ou d’autres éléments sur le graphique.
-   Utilisez une [*fréquence d’images*](wmformat-glossary.md)plus lente. Les captures d’écran peuvent souvent être efficaces à des fréquences d’images très basses (parfois jusqu’à 4 ou 5 images par seconde).
-   Réduisez la vitesse de transmission de l’audio qui l’accompagne.

En outre, le codec ne prend pas en charge le redimensionnement du rectangle vidéo. En d’autres termes, si vous essayez d’utiliser le codec pour encoder un écran 800 x 600 dans un rectangle vidéo 640 x 480, la vidéo obtenue aura des artefacts significatifs qui peuvent rendre illisible la grande partie du texte sur l’écran.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de la capture d’écran Flux**](configuring-screen-capture-streams.md)
</dt> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> </dl>

 

 




