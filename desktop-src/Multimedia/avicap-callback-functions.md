---
title: Fonctions de rappel AVICap
description: Fonctions de rappel AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- AVICap, classe, fonctions de rappel
- Fonctions de rappel AVICap, à propos de
- Message WM_CAP_SET_CALLBACK_CAPCONTROL
- Message WM_CAP_SET_CALLBACK_ERROR
- Message WM_CAP_SET_CALLBACK_FRAME
- Message WM_CAP_SET_CALLBACK_STATUS
- Message WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Message WM_CAP_SET_CALLBACK_WAVESTREAM
- Message WM_CAP_SET_CALLBACK_YIELD
- capSetCallbackOnCapControl macro)
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame macro)
- capSetCallbackOnStatus macro)
- capSetCallbackOnVideoStream macro)
- capSetCallbackOnWaveStream macro)
- capSetCallbackOnYield macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368671"
---
# <a name="avicap-callback-functions"></a>Fonctions de rappel AVICap

Votre application peut inscrire des fonctions de rappel avec une fenêtre de capture pour qu’elle notifie votre application lorsque l’état change, lorsque des erreurs se produisent, lorsque des mémoires tampons audio et vidéo sont disponibles, ainsi que pour le rendement pendant la capture en continu. Les messages suivants définissent la fonction de rappel.



| Message                                                                        | Description                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Cap \_ Set \_ callback \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | Spécifie la fonction de rappel dans l’application appelée pour fournir un contrôle précis sur le début et la fin de la capture. Vous pouvez également utiliser la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) pour envoyer ce message.                   |
| [**erreur de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-error.md)             | Spécifie la fonction de rappel dans l’application appelée lorsqu’une erreur se produit. Vous pouvez également utiliser la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) pour envoyer ce message.                                                           |
| [**FRAME de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-frame.md)             | Spécifie la fonction de rappel dans l’application appelée lorsque des frames d’aperçu sont capturés. Vous pouvez également utiliser la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) pour envoyer ce message.                                               |
| [**État de rappel de l' \_ ensemble de connexions WM \_ \_ \_**](wm-cap-set-callback-status.md)           | Spécifie la fonction de rappel dans l’application appelée lorsque l’état change. Vous pouvez également utiliser la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) pour envoyer ce message.                                                      |
| [**WM \_ Cap \_ Set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md) | Spécifie la fonction de rappel dans l’application appelée pendant la capture en continu lorsqu’une nouvelle mémoire tampon vidéo est disponible. Vous pouvez également utiliser la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) pour envoyer ce message. |
| [**WM \_ Cap \_ Set \_ callback \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)   | Spécifie la fonction de rappel dans l’application appelée pendant la capture en continu lorsqu’une nouvelle mémoire tampon audio est disponible. Vous pouvez également utiliser la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) pour envoyer ce message.   |
| [**\_jeu de \_ \_ rappels de la définition du jeu WM \_**](wm-cap-set-callback-yield.md)             | Spécifie la fonction de rappel dans l’application appelée lors de la création de la capture en continu. Vous pouvez également utiliser la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) pour envoyer ce message.                                         |



 

Les rubriques suivantes décrivent les différentes fonctions de rappel, les notifications envoyées aux fonctions et leurs utilisations.

 

 




