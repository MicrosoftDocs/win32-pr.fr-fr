---
title: Inversion de la lecture
description: Inversion de la lecture
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379907"
---
# <a name="reversing-playback"></a>Inversion de la lecture

Certains appareils prennent en charge la lecture dans le sens inverse. Vous pouvez lire le contenu d’un tel appareil dans le sens inverse à l’aide de la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) . Cette macro définit l’étendue de lecture à partir de la position de lecture actuelle jusqu’au début du contenu. Périphérique vidéo numérique, MCIAVI. DRV peut lire en arrière. Les appareils qui ne peuvent pas jouer en arrière, tels que les CD audio, peuvent émettre un message d’erreur lorsque **MCIWndPlayReverse** est appelé.

 

 




