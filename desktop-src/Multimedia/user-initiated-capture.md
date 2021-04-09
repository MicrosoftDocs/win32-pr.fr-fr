---
title: Capture de User-Initiated
description: Capture de User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840509"
---
# <a name="user-initiated-capture"></a><span data-ttu-id="65c66-105">Capture de User-Initiated</span><span class="sxs-lookup"><span data-stu-id="65c66-105">User-Initiated Capture</span></span>

<span data-ttu-id="65c66-106">Vous pouvez récupérer la valeur actuelle de l’indicateur de capture initié par l’utilisateur à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de bits WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="65c66-106">You can retrieve the current value of the user-initiated capture flag by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="65c66-107">La valeur de l’indicateur est stockée dans le membre **fMakeUserHitOKToCapture** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="65c66-107">The value of the flag is stored in the **fMakeUserHitOKToCapture** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="65c66-108">Vous pouvez fournir à l’utilisateur un contrôle précis sur le moment où démarrer une session de capture en affectant à ce membre la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="65c66-108">You can provide the user with precise control over when to start a capture session by setting this member to **TRUE**.</span></span> <span data-ttu-id="65c66-109">AVICap affiche une boîte de dialogue après avoir alloué toutes les mémoires tampons vidéo et audio pour une session de capture.</span><span class="sxs-lookup"><span data-stu-id="65c66-109">AVICap displays a dialog box after allocating all video and audio buffers for a capture session.</span></span> <span data-ttu-id="65c66-110">Cela permet à l’utilisateur d’éliminer les retards de capture en raison de l’initialisation du logiciel.</span><span class="sxs-lookup"><span data-stu-id="65c66-110">This lets the user eliminate capture delays because of software initialization.</span></span> <span data-ttu-id="65c66-111">Si votre application utilise un petit nombre de mémoires tampons vidéo, cette boîte de dialogue n’est probablement pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="65c66-111">If your application uses a small number of video buffers, this dialog box is probably unnecessary.</span></span> <span data-ttu-id="65c66-112">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="65c66-112">The default value is **FALSE**.</span></span>

 

 




