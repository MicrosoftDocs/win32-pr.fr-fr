---
title: Message WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEOCOMPRESSION affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner un compresseur à utiliser pendant le processus de capture.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- Message WM_CAP_DLG_VIDEOCOMPRESSION Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032829"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="035ce-104">\_Message WM Cap \_ DLG \_ VIDEOCOMPRESSION</span><span class="sxs-lookup"><span data-stu-id="035ce-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="035ce-105">Le message **WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION** affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner un compresseur à utiliser pendant le processus de capture.</span><span class="sxs-lookup"><span data-stu-id="035ce-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="035ce-106">La liste des compresseurs disponibles peut varier en fonction du format vidéo sélectionné dans la boîte de dialogue Format vidéo du pilote de capture.</span><span class="sxs-lookup"><span data-stu-id="035ce-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="035ce-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="035ce-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="035ce-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="035ce-108">Return Value</span></span>

<span data-ttu-id="035ce-109">Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="035ce-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="035ce-110">Notes</span><span class="sxs-lookup"><span data-stu-id="035ce-110">Remarks</span></span>

<span data-ttu-id="035ce-111">Utilisez ce message avec des pilotes de capture qui fournissent des frames uniquement au \_ format RGB de bi.</span><span class="sxs-lookup"><span data-stu-id="035ce-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="035ce-112">Ce message est particulièrement utile dans l’opération de capture d’étape pour combiner la capture et la compression en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="035ce-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="035ce-113">La compression des frames avec un compresseur logiciel dans le cadre d’une opération de capture en temps réel est probablement trop longue.</span><span class="sxs-lookup"><span data-stu-id="035ce-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="035ce-114">La compression n’affecte pas les frames copiés dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="035ce-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="035ce-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="035ce-115">Requirements</span></span>



| <span data-ttu-id="035ce-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="035ce-116">Requirement</span></span> | <span data-ttu-id="035ce-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="035ce-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="035ce-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="035ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="035ce-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="035ce-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="035ce-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="035ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="035ce-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="035ce-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="035ce-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="035ce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="035ce-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="035ce-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="035ce-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="035ce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="035ce-125">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="035ce-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="035ce-126">Messages de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="035ce-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





