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
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368895"
---
# <a name="specifying-time-formats"></a>Spécification des formats d’heure

Les types de données multimédias peuvent généralement utiliser le temps pour identifier des positions importantes dans leur contenu. Les formats d’heure courants sont les millisecondes, les pistes et les frames. d’autres formats d’heure moins courants, tels que SMPTE (la société de motion et les ingénieurs de télévision) 24, existent également. L’heure correspond au format et au système de référence pour les données audio Waveform, audio, MIDI et CD. La vidéo prend en charge l’heure même si elle est enregistrée sous la forme d’une séquence de trames (flux) qui est généralement jouée à une vitesse spécifique. Plusieurs macros sont disponibles pour désigner le format d’heure.

Vous pouvez récupérer le format d’heure actuel d’un fichier ou d’un périphérique à l’aide de la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) . Vous pouvez modifier le format d’heure actuel en utilisant un autre format d’heure pris en charge par un appareil à l’aide de la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) . Ou vous pouvez définir le format d’heure sur millisecondes ou frames à l’aide des macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) ou [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .

> [!Note]  
> Les formats incontinus, tels que Tracks et SMPTE, peuvent entraîner un comportement anormal de la barre d’outils. Pour ces formats d’heure, vous souhaiterez peut-être désactiver la barre d’outils en spécifiant le \_ style de fenêtre MCIWNDF NOPLAYBAR lors de la création d’une fenêtre MCIWnd.

 

 

 




