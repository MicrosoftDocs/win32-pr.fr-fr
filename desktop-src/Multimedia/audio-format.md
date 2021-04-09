---
title: Format audio
description: Format audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- Message WM_CAP_GET_AUDIOFORMAT
- capGetAudioFormat macro)
- capGetAudioFormatSize macro)
- Message WM_CAP_SET_AUDIOFORMAT
- capSetAudioFormat macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842146"
---
# <a name="audio-format"></a>Format audio

Vous pouvez récupérer le format de capture actuel pour les données audio ou la taille de la structure du format audio en envoyant le message [**WM \_ Cap \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) (ou les macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) et [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) à une fenêtre de capture. Le format de capture audio par défaut est mono, binaire 8 bits, 11 kHz PCM (Pulse Code Modulation). Lorsque vous récupérez le format à l’aide de WM \_ Cap \_ obtenir \_ AUDIOFORMAT, utilisez toujours la structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) .

Vous pouvez définir le format de capture pour les données audio en envoyant le message [**WM \_ Cap \_ Set \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) (ou la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) ) à une fenêtre de capture. Lorsque vous définissez le format audio, vous pouvez passer un pointeur vers une structure [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX** ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , selon le format audio spécifié.

 

 