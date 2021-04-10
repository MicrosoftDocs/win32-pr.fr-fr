---
title: Limite de temps
description: Limite de temps
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- CAPTUREPARMS, structure
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- CAPTUREPARMS, structure
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675826"
---
# <a name="time-limit"></a><span data-ttu-id="c7de8-109">Limite de temps</span><span class="sxs-lookup"><span data-stu-id="c7de8-109">Time Limit</span></span>

<span data-ttu-id="c7de8-110">Vous pouvez limiter la durée d’une opération de capture à l’aide des membres **fLimitEnabled** et **wTimeLimit** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="c7de8-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="c7de8-111">Le membre **fLimitEnabled** indique si l’opération de capture doit être chronométrée, tandis que **wTimeLimit** spécifie la durée maximale de l’opération de capture.</span><span class="sxs-lookup"><span data-stu-id="c7de8-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="c7de8-112">Vous pouvez récupérer les valeurs de **fLimitEnabled** et **wTimeLimit** à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de la limite WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="c7de8-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="c7de8-113">Vous pouvez activer un minuteur pour l’opération de capture en spécifiant **true** comme valeur de **fLimitEnabled**, ou vous pouvez définir la durée de l’opération de capture en spécifiant une valeur, en secondes, pour **wTimeLimit**.</span><span class="sxs-lookup"><span data-stu-id="c7de8-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="c7de8-114">Après avoir défini ces membres, envoyez la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="c7de8-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="c7de8-115">La valeur par défaut de **fLimitEnabled** est **false**.</span><span class="sxs-lookup"><span data-stu-id="c7de8-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 




