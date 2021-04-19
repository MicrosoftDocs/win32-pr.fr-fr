---
description: Source de fichier AVI/WAV
ms.assetid: b8abf5d8-ba7f-441d-beef-9f85859318d5
title: Source de fichier AVI/WAV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef659d880ef570176f94ac91875291ea9d200cf5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517387"
---
# <a name="aviwav-file-source"></a>Source de fichier AVI/WAV

(Déconseillé. Pour les fichiers AVI et WAV, utilisez la [source de fichier (Async)](file-source--async--filter.md) et le [séparateur AVI](avi-splitter-filter.md) ou l' [analyseur Wave](wave-parser-filter.md).)

Le filtre de source de fichier AVI/WAV lit les fichiers sources AVI et WAV et génère les broches de sortie appropriées pour le type de fichier.

Pour les fichiers WAV, le filtre crée une broche de sortie audio qui produit un flux audio qui peut être connecté à un filtre de rendu audio ou un filtre de transformation audio intermédiaire.

Pour les fichiers AVI, le filtre crée une broche de sortie vidéo qui produit un flux AVI compressé adapté au filtre de codec AVI, et une broche de sortie audio qui produit un flux audio adapté à un filtre de rendu audio ou à un filtre de transformation audio intermédiaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



