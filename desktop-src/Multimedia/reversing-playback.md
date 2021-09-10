---
title: Inversion de la lecture
description: Inversion de la lecture
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369260"
---
# <a name="reversing-playback"></a>Inversion de la lecture

Certains appareils prennent en charge la lecture dans le sens inverse. Vous pouvez lire le contenu d’un tel appareil dans le sens inverse à l’aide de la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) . Cette macro définit l’étendue de lecture à partir de la position de lecture actuelle jusqu’au début du contenu. Périphérique vidéo numérique, MCIAVI. DRV peut lire en arrière. Les appareils qui ne peuvent pas jouer en arrière, tels que les CD audio, peuvent émettre un message d’erreur lorsque **MCIWndPlayReverse** est appelé.

 

 




