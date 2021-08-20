---
title: Utilisation de messages de fenêtre pour gérer Waveform-Audio enregistrement
description: Utilisation de messages de fenêtre pour gérer Waveform-Audio enregistrement
ms.assetid: 65637d51-9d30-48db-8681-48332442130e
keywords:
- audio Wave, gestion de l’enregistrement avec des messages
- Waveform-interface audio, gestion de l’enregistrement à l’aide de messages
- enregistrement de la forme d’onde audio, gestion de l’enregistrement avec les messages
- sons Waveform, messages
- Waveform-interface audio, messages
- enregistrement de la forme d’onde audio, messages
- Message MM_WIM_CLOSE
- Message MM_WIM_DATA
- Message MM_WIM_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c709df27be25a8a3f4c5a9be6528e28b4e8bab9251b04b6c397a7ef3fc8efd9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135651"
---
# <a name="using-window-messages-to-manage-waveform-audio-recording"></a>Utilisation de messages de fenêtre pour gérer Waveform-Audio enregistrement

Les messages suivants peuvent être envoyés à une fonction de procédure de fenêtre pour la gestion de l’enregistrement Waveform-Audio.



| Message                                | Description                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_fermeture de Wim de mm \_**](mm-wim-close.md) | Envoyé lorsque l’appareil est fermé à l’aide de la fonction [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose) .                                     |
| [**\_données Wim \_ mm**](mm-wim-data.md)   | Envoyé lorsque le pilote de périphérique est terminé avec une mémoire tampon envoyée à l’aide de la fonction [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) . |
| [**fichier \_ Wim \_ Open**](mm-wim-open.md)   | Envoyé lorsque l’appareil est ouvert à l’aide de la fonction [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) .                                       |



 

Le paramètre *lParam* des [**\_ \_ données Wim mm**](mm-wim-data.md) spécifie un pointeur vers une structure [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) qui identifie la mémoire tampon. Il se peut que cette mémoire tampon ne soit pas entièrement remplie avec des données Waveform-Audio ; l’enregistrement peut s’arrêter avant que la mémoire tampon ne soit remplie. Utilisez le membre **dwBytesRecorded** de la structure **WAVEHDR** pour déterminer la quantité de données valides présentes dans la mémoire tampon.

Le message le plus utile est probablement de [**mm \_ \_ données Wim**](mm-wim-data.md). Lorsque votre application se termine à l’aide du bloc de données envoyé par le pilote de périphérique, vous pouvez nettoyer et libérer le bloc de données. À moins que vous n’ayez besoin d’allouer de la mémoire ou d’initialiser des variables, vous n’avez probablement pas besoin d’utiliser les messages d' [**\_ \_ ouverture**](mm-wim-open.md) et de [**\_ \_ fermeture**](mm-wim-close.md) Wim de mm.

La fonction de rappel pour les périphériques d’entrée Waveform-Audio est fournie par l’application. Pour plus d’informations sur cette fonction de rappel, consultez la fonction [**waveInProc**](/previous-versions//dd743849(v=vs.85)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Enregistrement de la forme d’onde](recording-waveform-audio.md)
</dt> </dl>

 

 