---
title: Démarrage, suspension et reprise de la lecture
description: Démarrage, suspension et reprise de la lecture
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay macro)
- MCIWndPause macro)
- MCIWndResume macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49977b9bc741c6b32ce0da0c0ae9f63bd875a24268a00bb4782cd71531a4ef31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688669"
---
# <a name="starting-pausing-and-resuming-playback"></a>Démarrage, suspension et reprise de la lecture

[**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) est la macro de lecture la plus générale. Cette macro vous permet de lire un fichier ou un appareil à partir de la position de lecture actuelle. La lecture continue jusqu’à la fin du contenu, sauf si elle est interrompue.

Vous pouvez interrompre temporairement un appareil qui est en train de fonctionner à l’aide de la macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Pour reprendre la lecture à partir de la position suspendue, utilisez la macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Certains appareils ne prennent pas en charge les commandes de suspension et de reprise. Ces appareils mappent généralement **MCIWndPause** à la macro [**MCIWndStop**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) , qui arrête la lecture ou l’enregistrement. Vous pouvez redémarrer un appareil qui ne prend pas en charge la suspension ou la reprise à l’aide de **MCIWndPlay**, qui démarre la lecture à partir de la position de lecture actuelle.

 

 




