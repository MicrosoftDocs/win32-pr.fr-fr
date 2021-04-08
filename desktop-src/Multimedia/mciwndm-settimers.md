---
title: Message MCIWNDM_SETTIMERS (VFW. h)
description: Le \_ message MCIWNDM SETTIMERS définit les périodes de mise à jour utilisées par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- Message MCIWNDM_SETTIMERS Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740236"
---
# <a name="mciwndm_settimers-message"></a><span data-ttu-id="8248b-104">\_Message MCIWNDM SETTIMERS</span><span class="sxs-lookup"><span data-stu-id="8248b-104">MCIWNDM\_SETTIMERS message</span></span>

<span data-ttu-id="8248b-105">Le message **MCIWNDM \_ SETTIMERS** définit les périodes de mise à jour utilisées par MCIWnd pour mettre à jour le TrackBar dans la fenêtre MCIWnd, mettre à jour les informations de position affichées dans la barre de titre de la fenêtre et envoyer des messages de notification à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="8248b-105">The **MCIWNDM\_SETTIMERS** message sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.</span></span> <span data-ttu-id="8248b-106">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="8248b-106">You can send this message explicitly or by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span>


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a><span data-ttu-id="8248b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8248b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8248b-108"><span id="active"></span><span id="ACTIVE"></span>*proactive*</span><span class="sxs-lookup"><span data-stu-id="8248b-108"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="8248b-109">Période de mise à jour utilisée par MCIWnd lorsqu’il s’agit de la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="8248b-109">Update period used by MCIWnd when it is the active window.</span></span> <span data-ttu-id="8248b-110">La valeur par défaut est 500 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8248b-110">The default value is 500 milliseconds.</span></span> <span data-ttu-id="8248b-111">Le stockage de cette valeur est limité à 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8248b-111">Storage for this value is limited to 16 bits.</span></span>

</dd> <dt>

<span data-ttu-id="8248b-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span><span class="sxs-lookup"><span data-stu-id="8248b-112"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="8248b-113">Période de mise à jour utilisée par MCIWnd lorsqu’il s’agit de la fenêtre inactive.</span><span class="sxs-lookup"><span data-stu-id="8248b-113">Update period used by MCIWnd when it is the inactive window.</span></span> <span data-ttu-id="8248b-114">La valeur par défaut est 2000 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8248b-114">The default value is 2000 milliseconds.</span></span> <span data-ttu-id="8248b-115">Le stockage de cette valeur est limité à 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8248b-115">Storage for this value is limited to 16 bits.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8248b-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8248b-116">Return Value</span></span>

<span data-ttu-id="8248b-117">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8248b-117">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8248b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8248b-118">Requirements</span></span>



| <span data-ttu-id="8248b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8248b-119">Requirement</span></span> | <span data-ttu-id="8248b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8248b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8248b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8248b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8248b-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8248b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8248b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8248b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8248b-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8248b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8248b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="8248b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8248b-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8248b-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8248b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8248b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8248b-128">**MCIWndSetTimers**</span><span class="sxs-lookup"><span data-stu-id="8248b-128">**MCIWndSetTimers**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





