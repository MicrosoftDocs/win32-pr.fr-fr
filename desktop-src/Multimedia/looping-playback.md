---
title: Lecture en boucle pour MCIWnd
description: Lecture en boucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9144cd17886ff9d6f59bc38311481335a9ae581e5464d7feda0e7fd1a4ec2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139290"
---
# <a name="looping-playback-for-mciwnd"></a>Lecture en boucle pour MCIWnd

MCIWnd prend en charge la lecture comme une boucle continue. Vous pouvez lire le contenu d’un fichier ou d’un appareil de façon répétée en tant que boucle à l’aide de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinaison avec le bouton de **lecture** dans la barre d’outils. L’appareil de lecture vidéo, MCIAVI, prend en charge les boucles de lecture. Pour déterminer si la lecture continue a été activée, utilisez la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .

 

 




