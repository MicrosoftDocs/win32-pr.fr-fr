---
description: Source de fichier AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Source de fichier AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8c99de9eed21afa716c4f3ee81a5d1cc4e9731739526f7c9531c758b30a22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689359"
---
# <a name="aviwav-file-source"></a>Source de fichier AVI/WAV

(Déconseillé. Pour les fichiers AVI et WAV, utilisez la [source de fichier (Async)](file-source--async--filter.md) et le [séparateur AVI](avi-splitter-filter.md) ou l' [analyseur Wave](wave-parser-filter.md).)

Le filtre de source de fichier AVI/WAV lit les fichiers sources AVI et WAV et génère les broches de sortie appropriées pour le type de fichier.

Pour les fichiers WAV, le filtre crée une broche de sortie audio qui produit un flux audio qui peut être connecté à un filtre de rendu audio ou un filtre de transformation audio intermédiaire.

Pour les fichiers AVI, le filtre crée une broche de sortie vidéo qui produit un flux AVI compressé adapté au filtre de codec AVI, et une broche de sortie audio qui produit un flux audio adapté à un filtre de rendu audio ou à un filtre de transformation audio intermédiaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



