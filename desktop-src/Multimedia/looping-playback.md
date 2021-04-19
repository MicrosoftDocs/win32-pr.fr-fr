---
title: Lecture en boucle pour MCIWnd
description: Lecture en boucle (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106530067"
---
# <a name="looping-playback-for-mciwnd"></a>Lecture en boucle pour MCIWnd

MCIWnd prend en charge la lecture comme une boucle continue. Vous pouvez lire le contenu d’un fichier ou d’un appareil de façon répétée en tant que boucle à l’aide de la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) en combinaison avec le bouton de **lecture** dans la barre d’outils. L’appareil de lecture vidéo, MCIAVI, prend en charge les boucles de lecture. Pour déterminer si la lecture continue a été activée, utilisez la macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .

 

 




