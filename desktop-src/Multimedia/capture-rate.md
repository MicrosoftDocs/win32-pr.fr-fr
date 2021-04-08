---
title: Taux de capture
description: Taux de capture
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- CAPTUREPARMS, structure
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029211"
---
# <a name="capture-rate"></a><span data-ttu-id="a6fe6-108">Taux de capture</span><span class="sxs-lookup"><span data-stu-id="a6fe6-108">Capture Rate</span></span>

<span data-ttu-id="a6fe6-109">Le taux de capture est le nombre de trames capturées chaque seconde d’une session de capture.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-109">The capture rate is the number of frames that are captured each second of a capture session.</span></span> <span data-ttu-id="a6fe6-110">Vous pouvez récupérer le taux de capture actuel à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="a6fe6-110">You can retrieve the current capture rate by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="a6fe6-111">Le taux de capture actuel est stocké dans le membre **dwRequestMicroSecPerFrame** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="a6fe6-111">The current capture rate is stored in the **dwRequestMicroSecPerFrame** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="a6fe6-112">Vous pouvez définir le taux de capture en spécifiant le nombre de microsecondes entre les frames successifs comme valeur de ce membre, puis en envoyant la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de l’ensemble de la plage WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="a6fe6-112">You can set the capture rate by specifying the number of microseconds between successive frames as the value of this member, then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="a6fe6-113">La valeur par défaut de **dwRequestMicroSecPerFrame** est 66667, qui correspond à 15 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="a6fe6-113">The default value of **dwRequestMicroSecPerFrame** is 66667, which corresponds to 15 frames per second.</span></span>

 

 




