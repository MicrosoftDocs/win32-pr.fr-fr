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
ms.openlocfilehash: 70bb1cfe1ed0f7ba6052fc1eb6af8fca8355d87d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463003"
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

 

 