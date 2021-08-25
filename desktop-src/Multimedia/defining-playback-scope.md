---
title: Définition de l’étendue de lecture
description: Définition de l’étendue de lecture
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom macro)
- MCIWndPlayTo macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853c74cc4115cee72e4253e339f934e73b8d8e7e223f1b91e9992969c4ce3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785419"
---
# <a name="defining-playback-scope"></a>Définition de l’étendue de lecture

MCIWnd fournit des macros qui vous permettent de définir l' *étendue* de lecture. L’étendue correspond à la partie de la lecture que vous souhaitez lire. Par exemple, vous pouvez lire le contenu à partir d’une position autre que la position de début à l’aide de la macro [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) . Cette macro passe à la position spécifiée, commence la lecture et continue jusqu’à la fin du contenu. De même, vous pouvez lire le contenu à un point de terminaison spécifié à l’aide de la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) . Cette macro démarre à la position de lecture actuelle et s’exécute jusqu’à ce qu’elle atteigne la position spécifiée ou que la fin du contenu soit atteinte, selon la première entrée.

En outre, vous pouvez définir à la fois les positions de début et de fin à l’aide de la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) . Cette macro se déplace à la position de départ spécifiée et s’exécute jusqu’à ce que la position de fin spécifiée ou la fin du contenu soit atteinte.

 

 




