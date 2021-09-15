---
description: Mémoires tampons de média
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Mémoires tampons de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530785"
---
# <a name="media-buffers"></a>Mémoires tampons de média

Une mémoire tampon de média est un objet COM qui gère un bloc de mémoire, généralement pour contenir des données multimédias. Les mémoires tampons de média sont utilisées pour déplacer des données d’un composant de pipeline à l’autre. La plupart des applications n’utilisent pas directement les mémoires tampons de média, car la session de média gère l’ensemble du flot de données entre les objets de pipeline. Vous devez utiliser des mémoires tampons de média si vous écrivez votre propre composant de pipeline, ou si vous utilisez un composant de pipeline directement sans la session multimédia.

Les mémoires tampons de média exposent l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . Cette interface est conçue pour lire ou écrire n’importe quel type de données. Les images vidéo non compressées nécessitent un traitement spécial, car elles peuvent être stockées dans des surfaces Direct3D situées dans la mémoire vidéo.

Cette section contient les rubriques suivantes :



| Rubrique                                                        | Description                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Utilisation des mémoires tampons de média](working-with-media-buffers.md) | Décrit le comportement général des mémoires tampons de média pour tous les types de média. |
| [Mémoires tampons vidéo non compressées](uncompressed-video-buffers.md) | Utilisation des mémoires tampons de média qui contiennent des images vidéo non compressées.  |
| [Mémoire tampon de surface DirectX](directx-surface-buffer.md)         | Décrit comment stocker une surface Direct3D dans une mémoire tampon de média.         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives de Media Foundation](media-foundation-primitives.md)
</dt> </dl>

 

 



