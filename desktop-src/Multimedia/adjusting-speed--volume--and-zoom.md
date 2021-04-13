---
title: Réglage de la vitesse, du volume et du zoom
description: Réglage de la vitesse, du volume et du zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed macro)
- MCIWndGetSpeed macro)
- MCIWndSetVolume macro)
- MCIWndGetVolume macro)
- MCIWndSetZoom macro)
- MCIWndGetZoom macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379983"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Réglage de la vitesse, du volume et du zoom

Les macros vitesse, volume et zoom fournissent les fonctionnalités des commandes **affichage**, **volume** et **Vitesse** du menu MCIWnd. Les macros décrites dans cette section sont généralement utilisées avec des vidéos et d’autres périphériques qui affichent des images pendant la lecture.

Certains appareils prennent en charge plusieurs modifications de vitesse de lecture. Vous pouvez définir la vitesse de lecture de ces périphériques à l’aide de la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) . Cette macro définit la vitesse de lecture sur 1000. Des valeurs plus élevées indiquent des vitesses plus rapides. Des valeurs inférieures indiquent des vitesses plus lentes.

Vous pouvez récupérer la vitesse de lecture actuelle à l’aide de la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) . Cette macro utilise les mêmes valeurs et la même plage que celles utilisées par **MCIWndSetSpeed**.

Certains appareils prennent en charge les modifications de volume. Vous pouvez ajuster ou définir le volume à l’aide de la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) . Cette macro définit le niveau de volume normal en tant que 1000. Des valeurs plus élevées indiquent des volumes plus forts. Les valeurs inférieures indiquent des volumes plus silencieux.

Vous pouvez récupérer le niveau de volume actuel à l’aide de la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) . Cette macro utilise les mêmes valeurs numériques et plages que celles utilisées par **MCIWndSetVolume**.

Pour les appareils qui utilisent une fenêtre de lecture, MCIWnd prend en charge une fonctionnalité de zoom qui définit la taille de l’image de lecture. Vous pouvez définir la taille de l’image de lecture à l’aide de la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) . La macro redéfinit la taille de l’image de lecture tout en conservant les proportions constantes de l’image. La valeur de zoom est définie sous la forme d’un pourcentage de la taille de l’image d’origine. Ainsi, 100 représente la taille d’image d’origine, 50 indique que l’image affichée est la moitié de sa taille d’origine et 200 indique que l’image affichée est deux fois sa taille d’origine.

Vous pouvez récupérer la valeur de zoom actuelle à l’aide de la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) . Cette macro utilise les mêmes valeurs et la même plage que celles utilisées par **MCIWndSetZoom**.

> [!Note]  
> Les pilotes audio et Waveform-Audio MCI standard ne prennent pas en charge les modifications de volume ou de vitesse.

 

 

 




