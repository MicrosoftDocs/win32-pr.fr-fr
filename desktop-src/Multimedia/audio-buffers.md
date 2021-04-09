---
title: Mémoires tampons audio
description: Mémoires tampons audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672318"
---
# <a name="audio-buffers"></a>Mémoires tampons audio

Vous pouvez contrôler la partie audio d’une opération de capture de trois manières :

-   Incluez ou excluez l’audio de l’opération de capture.
-   Demander un nombre spécifique de mémoires tampons audio.
-   Demandez que les tampons audio soient d’une taille spécifique.

Vous pouvez récupérer les paramètres des mémoires tampons audio à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’extrémité de l’opération WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Le membre **fCaptureAudio** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) spécifie si l’audio est inclus ou exclu de l’opération de capture. Le nombre demandé actuel de mémoires tampons audio est stocké dans le membre **wNumAudioRequested** et la taille de la mémoire tampon audio actuelle est stockée dans le membre **dwAudioBufferSize** . Vous pouvez spécifier s’il faut inclure la capture audio, spécifier la taille et le nombre de mémoires tampons audio en mettant à jour ces membres, puis envoyer la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

Par défaut, l’audio est inclus dans l’opération de capture et les quatre mémoires tampons audio sont allouées. La valeur par défaut de **fCaptureAudio** est **true**. La taille de la mémoire tampon par défaut (la valeur de **dwAudioBufferSize**) peut contenir 0,5 secondes de données audio ou 10 Ko, la valeur la plus élevée étant retenue.

 

 




