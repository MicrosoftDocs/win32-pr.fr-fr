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
ms.openlocfilehash: 46a6493d22a495a56084e89d2b067c1cf9a874752b44b81f636b5a184b895199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687689"
---
# <a name="video-buffers"></a>Mémoires tampons vidéo

Les mémoires tampons utilisées avec la capture vidéo résident dans le segment de mémoire. Le nombre de mémoires tampons utilisées dans une opération de capture peut varier et dépendre de la valeur du membre **wNumVideoRequested** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) et de la mémoire système disponible.

Vous pouvez récupérer la valeur actuelle des tampons vidéo demandés à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Le nombre demandé actuel de mémoires tampons vidéo est stocké dans le membre **wNumVideoRequested** de la structure **CAPTUREPARMS** . Vous pouvez demander le placement et le nombre de mémoires tampons en mettant à jour ce membre, puis en envoyant la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

 

 




