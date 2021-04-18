---
title: Paramètres de capture vidéo
description: Paramètres de capture vidéo
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- CAPTUREPARMS, structure
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512025"
---
# <a name="video-capture-settings"></a><span data-ttu-id="b558b-108">Paramètres de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="b558b-108">Video Capture Settings</span></span>

<span data-ttu-id="b558b-109">La structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contient les paramètres de contrôle pour la capture vidéo en continu.</span><span class="sxs-lookup"><span data-stu-id="b558b-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="b558b-110">Cette structure contrôle plusieurs aspects du processus de capture et vous permet d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b558b-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="b558b-111">Spécifiez la fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="b558b-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="b558b-112">Spécifiez le nombre de mémoires tampons vidéo allouées.</span><span class="sxs-lookup"><span data-stu-id="b558b-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="b558b-113">Désactivez et activez la capture audio.</span><span class="sxs-lookup"><span data-stu-id="b558b-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="b558b-114">Spécifiez l’intervalle de temps pour la capture.</span><span class="sxs-lookup"><span data-stu-id="b558b-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="b558b-115">Spécifiez si un périphérique MCI (VCR ou videodisc) est utilisé lors de la capture.</span><span class="sxs-lookup"><span data-stu-id="b558b-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="b558b-116">Spécifiez le contrôle du clavier ou de la souris pour terminer la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="b558b-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="b558b-117">Spécifiez le type de moyenne vidéo appliqué pendant la capture.</span><span class="sxs-lookup"><span data-stu-id="b558b-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="b558b-118">Vous pouvez récupérer les paramètres de capture actuels dans la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en envoyant le message [**\_ \_ \_ \_ d’installation de la séquence WM**](wm-cap-get-sequence-setup.md) (ou la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="b558b-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="b558b-119">Vous pouvez définir un ou plusieurs paramètres de capture actuels en mettant à jour les membres appropriés de la structure **CAPTUREPARMS** , puis en envoyant le message [**\_ \_ \_ \_ d’installation de la séquence de l’ensemble WM Cap**](wm-cap-set-sequence-setup.md) (ou la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) et **CAPTUREPARMS** à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="b558b-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 




