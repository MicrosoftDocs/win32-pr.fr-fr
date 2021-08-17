---
description: décrit les statistiques que vous pouvez récupérer à partir d’un codec de média Windows.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Obtention des statistiques d’encodage (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa718a27894ea3e91faa953cb7b23e6c92b57c93d4b0fc0cf2c15b6995f28b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449159"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a>Obtention des statistiques d’encodage (Microsoft Media Foundation)

Les informations relatives à ce qui se passe dans une session d’encodage sont généralement immédiatement disponibles sous la forme de codes d’erreur retournés lors du traitement des exemples. Toutefois, il existe des statistiques que vous pouvez récupérer à partir du codec sur différents aspects d’encodage.

## <a name="video-frame-information"></a>Informations sur les trames vidéo

Certaines statistiques vidéo que vous pouvez récupérer avec le nombre de trames traitées par l’encodeur. Il existe trois propriétés de nombre d’images que vous pouvez lire à partir de l’encodeur vidéo :

-   [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) est le nombre de frames traités par le biais du flux d’entrée de l’DMO.
-   [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) est le nombre de trames encodées. En soustrayant cette valeur du nombre total de frames passés, vous pouvez déterminer le nombre de frames qui ont été supprimés.
-   [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) est le nombre de trames qui ne sont pas encodées, car il s’agit déjà d’un contenu dupliqué. Cette valeur n’est pas soustraite du nombre d’images codées signalées par le DMO.

Vous pouvez lire les propriétés de l’image vidéo à tout moment pendant l’encodage. Cela peut être utile pour déterminer si les paramètres d’encodage sont adaptés à votre contenu. s’il existe une grande différence entre les trames totales et les trames codées, le contenu compressé peut ne pas répondre à vos besoins en matière de qualité. Vous pouvez lire les valeurs finales une fois l’encodage terminé.

## <a name="vbr-buffer-statistics"></a>Statistiques du tampon VBR

En fonction du mode d’encodage utilisé, une partie ou la totalité des paramètres de la mémoire tampon peut être déterminée lors de l’encodage (par exemple, la vitesse de transmission du VBR basé sur la qualité n’est pas connue tant que le contenu n’est pas encodé). Il existe quatre propriétés de mémoire tampon VBR que vous pouvez obtenir à l’aide de la méthode **IPropertyBag :: Read** :

-   [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) est la vitesse de transmission moyenne du contenu VBR.
-   [MFPKEY \_ BAVG](mfpkey-bavgproperty.md) est la fenêtre de mémoire tampon pour la vitesse de transmission moyenne.
-   [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) est le taux binaire de pointe du contenu VBR.
-   [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) est la fenêtre de mémoire tampon de pointe.

Une fois que vous avez commencé le traitement des exemples, vous ne devez pas lire les propriétés VBR tant que vous n’avez pas terminé d’encoder le flux. Si vous le faites, l’encodeur interprète votre demande comme un signal indiquant que l’encodage est terminé. L’exemple suivant que vous traitez est traité comme une nouvelle session d’encodage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codecs Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



