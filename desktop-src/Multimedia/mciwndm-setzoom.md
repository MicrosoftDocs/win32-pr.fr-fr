---
title: Message MCIWNDM_SETZOOM (VFW. h)
description: Le \_ message MCIWNDM SETZOOM redimensionne une image vidéo en fonction d’un facteur de zoom. Ce Marco ajuste la taille d’une fenêtre MCIWnd tout en conservant les proportions constantes. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- Message MCIWNDM_SETZOOM Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464507"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="e48c3-106">\_Message MCIWNDM SETZOOM</span><span class="sxs-lookup"><span data-stu-id="e48c3-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="e48c3-107">Le message **MCIWNDM \_ SETZOOM** redimensionne une image vidéo en fonction d’un facteur de zoom.</span><span class="sxs-lookup"><span data-stu-id="e48c3-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="e48c3-108">Ce Marco ajuste la taille d’une fenêtre MCIWnd tout en conservant les proportions constantes.</span><span class="sxs-lookup"><span data-stu-id="e48c3-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="e48c3-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="e48c3-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="e48c3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e48c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e48c3-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span><span class="sxs-lookup"><span data-stu-id="e48c3-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="e48c3-112">Facteur de zoom exprimé sous la forme d’un pourcentage de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="e48c3-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="e48c3-113">Spécifiez 100 pour afficher l’image à sa taille d’auteur, 200 pour afficher l’image au double de sa taille normale, ou 50 pour afficher l’image à la moitié de sa taille normale.</span><span class="sxs-lookup"><span data-stu-id="e48c3-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e48c3-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e48c3-114">Return Value</span></span>

<span data-ttu-id="e48c3-115">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e48c3-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e48c3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e48c3-116">Requirements</span></span>



| <span data-ttu-id="e48c3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e48c3-117">Requirement</span></span> | <span data-ttu-id="e48c3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e48c3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e48c3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e48c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e48c3-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e48c3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e48c3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e48c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e48c3-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e48c3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e48c3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e48c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e48c3-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48c3-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48c3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e48c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48c3-126">**MCIWndSetZoom**</span><span class="sxs-lookup"><span data-stu-id="e48c3-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





