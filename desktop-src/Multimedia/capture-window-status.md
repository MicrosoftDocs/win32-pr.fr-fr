---
title: État de la fenêtre de capture
description: État de la fenêtre de capture
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Message WM_CAP_GET_STATUS
- capGetStatus macro)
- CAPSTATUS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029604"
---
# <a name="capture-window-status"></a><span data-ttu-id="83656-106">État de la fenêtre de capture</span><span class="sxs-lookup"><span data-stu-id="83656-106">Capture Window Status</span></span>

<span data-ttu-id="83656-107">Vous pouvez récupérer l’état actuel d’une fenêtre de capture à l’aide du message d' [**\_ \_ \_ État WM Cap obtenir**](wm-cap-get-status.md) (ou la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ).</span><span class="sxs-lookup"><span data-stu-id="83656-107">You can retrieve the current status of a capture window by using the [**WM\_CAP\_GET\_STATUS**](wm-cap-get-status.md) message (or the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro).</span></span> <span data-ttu-id="83656-108">Ce message récupère une copie de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) avec les valeurs actuelles de ses membres.</span><span class="sxs-lookup"><span data-stu-id="83656-108">This message retrieves a copy of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure with the current values of its members.</span></span> <span data-ttu-id="83656-109">La structure **CAPSTATUS** contient des informations sur les dimensions de l’image, la position de défilement et si la superposition ou l’aperçu de l’image est activé.</span><span class="sxs-lookup"><span data-stu-id="83656-109">The **CAPSTATUS** structure contains information regarding the dimensions of the image, scroll position, and whether overlay or preview of the image is enabled.</span></span> <span data-ttu-id="83656-110">Étant donné que les informations représentées dans **CAPSTATUS** sont dynamiques, votre application doit actualiser le contenu de la structure chaque fois que la taille ou le format du flux vidéo capturé peut avoir changé (par exemple, après avoir affiché le format vidéo du pilote de capture).</span><span class="sxs-lookup"><span data-stu-id="83656-110">Because the information represented in **CAPSTATUS** is dynamic, your application should refresh the contents of the structure whenever the size or format of the captured video stream might have changed (such as after displaying the video format of the capture driver).</span></span>

<span data-ttu-id="83656-111">La modification des dimensions de la fenêtre de capture n’a aucun effet sur les dimensions du flux vidéo capturé réel.</span><span class="sxs-lookup"><span data-stu-id="83656-111">Changing the dimensions of the capture window has no effect on the dimensions of the actual captured video stream.</span></span> <span data-ttu-id="83656-112">La boîte de dialogue Format affichée par le pilote de périphérique de capture vidéo contrôle les dimensions du flux vidéo capturé.</span><span class="sxs-lookup"><span data-stu-id="83656-112">The format dialog box displayed by the video capture device driver controls the dimensions of the captured video stream.</span></span>

 

 




