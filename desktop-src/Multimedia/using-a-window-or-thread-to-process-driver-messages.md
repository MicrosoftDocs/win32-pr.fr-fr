---
title: Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote
description: Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- audio Wave, rappel de fenêtre
- blocs de données audio, rappel de fenêtre
- audio Wave, rappel de thread
- blocs de données audio, rappel de thread
- audio Wave, traitement des messages de pilote
- blocs de données audio, traitement des messages de pilote
- traitement des messages du pilote
- waveInOpen fonction)
- waveOutOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367695"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a>Utilisation d’une fenêtre ou d’un thread pour traiter des messages de pilote

Pour utiliser une fonction de rappel de fenêtre, spécifiez l' \_ indicateur de fenêtre de rappel dans le paramètre *fdwOpen* et un handle de fenêtre dans le mot de poids faible du paramètre *DwCallback* de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) ou [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) . Les messages du pilote seront envoyés à la procédure de fenêtre pour la fenêtre identifiée par le descripteur dans *dwCallback*.

De même, pour utiliser un rappel de thread, spécifiez \_ le thread de rappel et un handle de thread dans l’appel à **WaveInOpen** ou **waveOutOpen**. Dans ce cas, les messages sont publiés dans le thread spécifié et non dans une fenêtre.

Les messages envoyés au rappel de la fenêtre ou du thread sont spécifiques au type de périphérique audio utilisé. Pour plus d’informations sur ces messages, consultez [playing Waveform-Audio Files](playing-waveform-audio-files.md).

 

 