---
title: Lecture en boucle pour MCIWnd
description: Lecture en boucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369111"
---
# <a name="looping-playback-for-mciwnd"></a>Lecture en boucle pour MCIWnd

MCIWnd prend en charge la lecture comme une boucle continue. Vous pouvez lire le contenu d’un fichier ou d’un appareil de façon répétée en tant que boucle à l’aide de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinaison avec le bouton de **lecture** dans la barre d’outils. L’appareil de lecture vidéo, MCIAVI, prend en charge les boucles de lecture. Pour déterminer si la lecture continue a été activée, utilisez la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .

 

 




