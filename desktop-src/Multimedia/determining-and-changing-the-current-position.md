---
title: Détermination et modification de la position actuelle
description: Détermination et modification de la position actuelle
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart macro)
- MCIWndGetEnd macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594aa63b4b620327cd8b9ae41c263c197e1a981405c2148545ae7b8d4df86c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497339"
---
# <a name="determining-and-changing-the-current-position"></a>Détermination et modification de la position actuelle

Lorsqu’un fichier ou un appareil est associé à une fenêtre MCIWnd, la position de lecture est initialement définie au début du contenu, quel que soit le type de support. Pendant la lecture, la position de lecture se déplace de manière linéaire dans le contenu et, si la lecture n’est pas interrompue, finit par atteindre la fin du contenu. Si une interruption se produit, la position de lecture actuelle est l’emplacement auquel la lecture a été arrêtée ou suspendue.

Vous pouvez récupérer les emplacements pour le début et la fin du contenu à l’aide des macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) et [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) . Vous pouvez déterminer la longueur du contenu en soustrayant la valeur retournée par **MCIWndGetStart** de la valeur retournée par **MCIWndGetEnd**, ou à l’aide de la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) . Vous pouvez récupérer la position de lecture actuelle à l’aide de la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) , ou vous pouvez récupérer la position de lecture comme une chaîne se terminant par un caractère null à l’aide de la macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .

Pour modifier la position de lecture actuelle, utilisez les macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)et [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) . Vous pouvez déplacer la position de lecture au début du contenu à l’aide de **MCIWndHome** ou à la fin du contenu à l’aide de **MCIWndEnd**. Utilisez **MCIWndSeek** pour déplacer la position de lecture vers n’importe quel emplacement du contenu.

Vous pouvez également parcourir le contenu à l’aide de la macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) . À partir de la position de lecture actuelle, cette macro déplace la position de lecture vers l’avant ou vers l’arrière d’un incrément spécifié.

> [!Note]  
> Les unités utilisées pour spécifier la position varient selon les différents types de médias et périphériques. Par exemple, la position de lecture pour les fichiers AVI utilisés par l’appareil MCIAVI est mesurée en frames. la position de lecture pour les fichiers audio CD, Waveform-Audio et MIDI est mesurée en millisecondes.

 

Les appareils pour d’autres types de supports et des appareils tiers peuvent utiliser d’autres unités. Pour plus d’informations sur la détermination de ces unités, consultez [améliorations de la lecture](playback-enhancements.md).

 

 




