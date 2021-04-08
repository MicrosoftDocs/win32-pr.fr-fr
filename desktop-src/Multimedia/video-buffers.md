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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674589"
---
# <a name="video-buffers"></a><span data-ttu-id="779ab-107">Mémoires tampons vidéo</span><span class="sxs-lookup"><span data-stu-id="779ab-107">Video Buffers</span></span>

<span data-ttu-id="779ab-108">Les mémoires tampons utilisées avec la capture vidéo résident dans le segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="779ab-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="779ab-109">Le nombre de mémoires tampons utilisées dans une opération de capture peut varier et dépendre de la valeur du membre **wNumVideoRequested** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) et de la mémoire système disponible.</span><span class="sxs-lookup"><span data-stu-id="779ab-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="779ab-110">Vous pouvez récupérer la valeur actuelle des tampons vidéo demandés à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="779ab-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="779ab-111">Le nombre demandé actuel de mémoires tampons vidéo est stocké dans le membre **wNumVideoRequested** de la structure **CAPTUREPARMS** .</span><span class="sxs-lookup"><span data-stu-id="779ab-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="779ab-112">Vous pouvez demander le placement et le nombre de mémoires tampons en mettant à jour ce membre, puis en envoyant la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="779ab-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 




