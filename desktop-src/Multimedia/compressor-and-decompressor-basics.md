---
title: Concepts de base du compresseur et du décompresseur
description: Concepts de base du compresseur et du décompresseur
ms.assetid: 49a958c1-1798-4c6c-913c-5bf5869f926b
keywords:
- Gestionnaire de compression vidéo (VCM), ouverture de compresseurs
- VCM (Video Compression Manager), ouverture de compresseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b51e0221c495d5e2d0782f4e56e0778c0d2462
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839937"
---
# <a name="compressor-and-decompressor-basics"></a>Concepts de base du compresseur et du décompresseur

Pour ouvrir et localiser un compresseur, vous pouvez utiliser les fonctions [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) et [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Vous pouvez utiliser **ICLocate** pour rechercher un compresseur d’un type spécifique et obtenir un handle de celui-ci en vue de son utilisation dans d’autres fonctions VCM. Pour ouvrir un compresseur, vous pouvez utiliser **ICOpen**. Votre application utilise le descripteur retourné par cette fonction pour identifier le compresseur ouvert lorsqu’il utilise d’autres fonctions VCM.

Pour ouvrir et localiser un décompresseur, les applications peuvent utiliser les macros [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen) et [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) . Ces macros utilisent **ICLocate** pour l’opération.

Lorsque votre application a terminé d’utiliser un compresseur ou un décompresseur, elle doit la fermer pour libérer toutes les ressources utilisées pour la compression ou la décompression. Votre application peut utiliser la fonction [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) pour fermer le compresseur ou le décompresseur.

En outre, votre application peut énumérer les compresseurs ou les décompresseurs sur un système à l’aide de la fonction [**ICInfo**](/windows/desktop/api/Vfw/nf-vfw-icinfo) .

> [!Note]  
> L’en-tête de flux d’un fichier AVI contient des informations sur le type de flux et le gestionnaire spécifique pour ce flux. Dans l’en-tête de flux, les membres **fccType** et **fccHandler** identifient le type de flux et le gestionnaire de flux spécifiés pour le flux.

 

 

 




