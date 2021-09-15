---
description: Encodage vidéo avec compression temporelle
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Encodage vidéo avec compression temporelle (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411495"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Encodage vidéo avec compression temporelle (Microsoft Media Foundation)

pour obtenir les taux de compression les plus élevés possibles, les codecs Windows Media Video utilisent la *compression temporelle*. La compression temporelle est une technique qui consiste à réduire la taille de la vidéo compressée en n’codant pas chaque frame en tant qu’image complète. Les frames encodés complètement (comme une image statique) sont appelés *images clés*. Toutes les autres images de la vidéo sont représentées par des données qui spécifient la modification depuis la dernière image. Ces frames sont appelés des *frames Delta*.

La quantité de compression qui peut être obtenue à l’aide de la compression temporelle dépend du contenu. Si la vidéo est statique, sans mouvement important ou autre modification dans l’image, de nombreuses images Delta peuvent être créées pour chaque image clé. Plus le nombre d’images Delta utilisées est élevé, plus le flux vidéo encodé est petit. Toutefois, si la vidéo est dynamique, avec un grand nombre de couleurs animées ou changeantes, l’avantage de l’utilisation de la compression temporelle est plus petit.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la vidéo](workingwithvideo.md)
</dt> </dl>

 

 



