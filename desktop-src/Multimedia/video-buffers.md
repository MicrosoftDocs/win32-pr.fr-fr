---
title: Mémoires tampons vidéo
description: Mémoires tampons vidéo
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368775"
---
# <a name="video-buffers"></a>Mémoires tampons vidéo

Les mémoires tampons utilisées avec la capture vidéo résident dans le segment de mémoire. Le nombre de mémoires tampons utilisées dans une opération de capture peut varier et dépendre de la valeur du membre **wNumVideoRequested** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) et de la mémoire système disponible.

Vous pouvez récupérer la valeur actuelle des tampons vidéo demandés à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Le nombre demandé actuel de mémoires tampons vidéo est stocké dans le membre **wNumVideoRequested** de la structure **CAPTUREPARMS** . Vous pouvez demander le placement et le nombre de mémoires tampons en mettant à jour ce membre, puis en envoyant la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

 

 




