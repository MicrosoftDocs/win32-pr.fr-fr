---
title: Préallocation d’espace disque pour le fichier de capture
description: Préallocation d’espace disque pour le fichier de capture
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- Message WM_CAP_FILE_ALLOCATE
- capFileAlloc macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309854"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Préallocation d’espace disque pour le fichier de capture

Préallouer de l’espace disque pour le fichier de capture crée un fichier d’une taille spécifiée sur le disque avant le démarrage d’une opération de capture. La préallocation d’un fichier de capture réduit le traitement nécessaire lorsque la capture est en cours et entraîne moins de frames supprimés. Vous pouvez préallouer un fichier de capture à l’aide du message d' [**\_ \_ \_ allocation de fichier WM Cap**](wm-cap-file-allocate.md) (ou de la macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).

En règle générale, votre application doit préallouer suffisamment d’espace disque pour contenir le plus grand fichier de capture prévu. La préallocation de l’espace disque ne limite pas la taille du fichier capturé. La taille du fichier est automatiquement augmentée si les données capturées dépassent l’espace alloué. Les opérations d’écriture ultérieures dans le fichier de capture réutilisent les portions d’espace disque allouées pour le fichier, ce qui permet de conserver la taille et la fragmentation du fichier.

Vous pouvez également améliorer les performances de capture en défragmentant le fichier de capture. Pour défragmenter le fichier, utilisez un utilitaire de défragmentation tel que le Défragmenteur de disque. Si vous utilisez un fichier de capture défragmenté et que vous l’agrandissez plus tard, vous devez défragmenter le fichier agrandi. L’agrandissement d’un fichier de capture défragmenté peut fragmenter la partie développée du fichier et réduire les performances de l’opération de capture.

Vous pouvez également améliorer les performances à l’aide d’un disque non compressé pour la capture vidéo. La compression des données pendant la capture peut limiter le débit des captures sur le disque.

Une application peut réserver un fichier de capture permanent pour éliminer le temps nécessaire à la préallocation et à la défragmentation d’un fichier chaque fois qu’il est démarré. Comme un fichier de capture peut nécessiter un espace disque considérable et que la préallocation d’un fichier de capture supprime toutes les données d’un fichier de capture existant, une application doit permettre à l’utilisateur de décider si le fichier est permanent ou temporaire.

 

 




