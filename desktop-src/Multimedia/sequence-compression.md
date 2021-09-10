---
title: Compression de séquence
description: Compression de séquence
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Gestionnaire de compression vidéo (VCM), compression de séquence
- VCM (gestionnaire de compression vidéo), compression de séquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369004"
---
# <a name="sequence-compression"></a>Compression de séquence

Votre application peut utiliser les fonctions [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)et [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) pour compresser une séquence de frames. Ces fonctions utilisent les données stockées dans la structure [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) . Les applications utilisent la fonction [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) pour permettre à l’utilisateur de sélectionner un compresseur, de l’ouvrir et de définir les paramètres de compression dans la structure **COMPVARS** . Toutefois, les applications peuvent définir manuellement les paramètres dans la structure.

Avant qu’une application puisse commencer à compresser une séquence de frames, elle doit utiliser **ICSeqCompressFrameStart** pour allouer les ressources nécessaires. Une fois les ressources allouées, l’application peut utiliser **ICSeqCompressFrame** pour compresser chaque frame individuellement. La fréquence d’images et la fréquence d’image clé utilisée pour compresser la séquence sont spécifiées dans les membres de la structure **COMPVARS** . La valeur de retour pour **ICSeqCompressFrame** pointe vers les données compressées.

Quand une application finit de compresser une séquence, elle peut utiliser **ICSeqCompressFrameEnd** pour libérer des ressources système allouées pour **ICSeqCompressFrameStart**. Pour libérer les ressources allouées pour la structure **COMPVARS** , l’application peut utiliser la fonction [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .

 

 




