---
title: Spécification des formats d’heure
description: Spécification des formats d’heure
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat macro)
- MCIWndSetTimeFormat macro)
- MCIWndUseTime macro)
- MCIWndUseFrames macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c14303879a3d13d018be8691eb1947ee1ed67907df796ae38cffc3936bf2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801702"
---
# <a name="specifying-time-formats"></a>Spécification des formats d’heure

Les types de données multimédias peuvent généralement utiliser le temps pour identifier des positions importantes dans leur contenu. Les formats d’heure courants sont les millisecondes, les pistes et les frames. d’autres formats d’heure moins courants, tels que SMPTE (la société de motion et les ingénieurs de télévision) 24, existent également. L’heure correspond au format et au système de référence pour les données audio Waveform, audio, MIDI et CD. La vidéo prend en charge l’heure même si elle est enregistrée sous la forme d’une séquence de trames (flux) qui est généralement jouée à une vitesse spécifique. Plusieurs macros sont disponibles pour désigner le format d’heure.

Vous pouvez récupérer le format d’heure actuel d’un fichier ou d’un périphérique à l’aide de la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) . Vous pouvez modifier le format d’heure actuel en utilisant un autre format d’heure pris en charge par un appareil à l’aide de la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) . Ou vous pouvez définir le format d’heure sur millisecondes ou frames à l’aide des macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) ou [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .

> [!Note]  
> Les formats incontinus, tels que Tracks et SMPTE, peuvent entraîner un comportement anormal de la barre d’outils. Pour ces formats d’heure, vous souhaiterez peut-être désactiver la barre d’outils en spécifiant le \_ style de fenêtre MCIWNDF NOPLAYBAR lors de la création d’une fenêtre MCIWnd.

 

 

 




