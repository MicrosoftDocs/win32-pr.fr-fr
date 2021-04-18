---
description: Cette rubrique explique comment effectuer une recherche au cours de la lecture à l’aide de MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Comment rechercher pendant la lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520405"
---
# <a name="how-to-seek-during-playback"></a>Comment rechercher pendant la lecture

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Cette rubrique explique comment effectuer une recherche au cours de la lecture à l’aide de MFPlay.

**Pour rechercher pendant la lecture**

1.  Initialisez un **PROPVARIANT** pour contenir le temps de recherche en unités de 100 nanosecondes, sous la forme d’un **grand \_ entier** (**VT \_ i8**).
2.  Appelez [**IMFPMediaPlayer :: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition). Spécifiez **MFP \_ POSITIONTYPE \_ 100 ns** pour le premier paramètre, puis transmettez le **PROPVARIANT** pour le deuxième paramètre.

## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



