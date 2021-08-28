---
title: Capture manuelle des frames
description: Capture manuelle des frames
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- Message WM_CAP_SINGLE_FRAME_OPEN
- Message WM_CAP_SINGLE_FRAME
- Message WM_CAP_SINGLE_FRAME_CLOSE
- capCaptureSingleFrameOpen macro)
- capCaptureSingleFrame macro)
- capCaptureSingleFrameClose macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9024f8759697248b1aadf2f46f902c4bf706c9d10417281d9b5c4f61fc1e94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138854"
---
# <a name="manual-frame-capture"></a>Capture manuelle des frames

Si vous souhaitez spécifier individuellement les frames à capturer dans un flux vidéo, vous pouvez contrôler la séquence à l’aide des messages de l' [**\_ \_ image unique WM embout \_ \_ Open**](wm-cap-single-frame-open.md), du [**\_ \_ \_ cadre unique WM**](wm-cap-single-frame.md)et du [**\_ \_ \_ \_ cadre unique WM Cap**](wm-cap-single-frame-close.md) (ou des macros [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)et [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ). En règle générale, ces messages sont utilisés pour créer une animation en ajoutant des frames individuels au fichier de capture. Le \_ \_ cadre unique WM Cap \_ \_ Open ouvre un fichier pour une opération de capture pilotée manuellement. \_ \_ Le frame WM embout unique \_ capture un frame individuel et l’ajoute au fichier de capture. \_ \_ \_ La fermeture de frame unique WM Cap \_ ferme le fichier utilisé pour la capture manuelle de frame.

> [!Note]  
> Cette méthode de capture ne prend pas en charge la capture audio simultanée avec capture vidéo.

 

 

 




