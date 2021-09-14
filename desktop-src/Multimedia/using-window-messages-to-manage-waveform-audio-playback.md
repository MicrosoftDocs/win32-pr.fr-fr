---
title: Utilisation de messages de fenêtre pour gérer Waveform-Audio lecture
description: Utilisation de messages de fenêtre pour gérer Waveform-Audio lecture
ms.assetid: 217968fd-4bb3-405d-a371-c129e29637ab
keywords:
- sons Waveform, gestion de la lecture avec les messages
- Waveform-interface audio, gestion de la lecture avec des messages
- lecture de fichiers Waveform-Audio, gestion de la lecture avec des messages
- sons Waveform, messages
- Waveform-interface audio, messages
- lecture des fichiers Waveform-Audio, messages
- Message MM_WOM_CLOSE
- Message MM_WOM_DONE
- Message MM_WOM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02794222274e10498e31e0f38939d930ef3745
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194915"
---
# <a name="using-window-messages-to-manage-waveform-audio-playback"></a>Utilisation de messages de fenêtre pour gérer Waveform-Audio lecture

Les messages suivants peuvent être envoyés à une fonction de procédure de fenêtre pour la gestion de la lecture Waveform-Audio.



| Message                                | Description                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ WOM \_ Fermer**](mm-wom-close.md) | Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) .                                 |
| [**MM \_ WOM \_ terminé**](mm-wom-done.md)   | Envoyé lorsque le pilote de périphérique est terminé avec un bloc de données envoyé à l’aide de la fonction [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . |
| [**MM \_ WOM \_ ouverts**](mm-wom-open.md)   | Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .                                   |



 

Un paramètre *wParam* et *lParam* est associé à chacun de ces messages. Le paramètre *wParam* spécifie toujours un handle du périphérique Wave-Audio ouvert. Pour le message [**mm \_ WOM \_ done**](mm-wom-done.md) , *lParam* spécifie un pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie le bloc de données terminé. Le paramètre *lParam* n’est pas utilisé pour les messages Open [**\_ WOM \_ Fermer**](mm-wom-close.md) et [**mm \_ WOM \_ Open**](mm-wom-open.md) .

Le message le plus utile est probablement de MM \_ WOM \_ . Lorsque ce message signale que la lecture d’un bloc de données est terminée, vous pouvez nettoyer et libérer le bloc de données. À moins que vous n’ayez besoin d’allouer de la mémoire ou d’initialiser des variables, vous n’avez probablement pas besoin de traiter les \_ \_ messages WOM Open et mm \_ WOM \_ Close.

La fonction de rappel pour les périphériques de sortie Waveform-Audio est fournie par l’application. Pour plus d’informations sur cette fonction de rappel, consultez la fonction [**waveOutProc**](/previous-versions//dd743869(v=vs.85)) .

 

 