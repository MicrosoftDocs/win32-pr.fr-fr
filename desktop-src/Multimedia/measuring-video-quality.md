---
title: Mesure de la qualité vidéo
description: Mesure de la qualité vidéo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029136"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="ac89c-107">Mesure de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="ac89c-107">Measuring Video Quality</span></span>

<span data-ttu-id="ac89c-108">Une façon de mesurer la qualité vidéo consiste à limiter le nombre de trames capturées supprimées pendant l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="ac89c-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="ac89c-109">Une fois la capture en continu terminée, la valeur de qualité est comparée au rapport entre les images supprimées et le nombre total de trames.</span><span class="sxs-lookup"><span data-stu-id="ac89c-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="ac89c-110">Si le pourcentage de frames supprimés est supérieur à la valeur du membre **wPercentDropForError** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap envoie un message d’erreur à la fonction de rappel d’erreur si elle est installée.</span><span class="sxs-lookup"><span data-stu-id="ac89c-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="ac89c-111">Vous pouvez récupérer la limite actuelle d’images supprimées (exprimées sous forme de pourcentage) à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="ac89c-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="ac89c-112">Vous pouvez définir une nouvelle limite en spécifiant un pourcentage comme valeur du membre **wPercentDropForError** de la structure **CAPTUREPARMS** , puis en envoyant la structure mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="ac89c-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="ac89c-113">La valeur par défaut de **wPercentDropForError** est 10 pour cent.</span><span class="sxs-lookup"><span data-stu-id="ac89c-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 




