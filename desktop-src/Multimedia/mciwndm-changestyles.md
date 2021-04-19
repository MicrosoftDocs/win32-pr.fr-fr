---
title: Message MCIWNDM_CHANGESTYLES (VFW. h)
description: Le \_ message MCIWNDM CHANGESTYLES modifie les styles utilisés par la fenêtre MCIWnd. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- Message MCIWNDM_CHANGESTYLES Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518063"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="181ca-105">\_Message MCIWNDM CHANGESTYLES</span><span class="sxs-lookup"><span data-stu-id="181ca-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="181ca-106">Le message **MCIWNDM \_ CHANGESTYLES** modifie les styles utilisés par la fenêtre MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="181ca-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="181ca-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .</span><span class="sxs-lookup"><span data-stu-id="181ca-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="181ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="181ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="181ca-109"><span id="mask"></span><span id="MASK"></span>*filtrage*</span><span class="sxs-lookup"><span data-stu-id="181ca-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="181ca-110">Masque qui identifie les styles qui peuvent changer.</span><span class="sxs-lookup"><span data-stu-id="181ca-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="181ca-111">Ce masque est l’opérateur or au niveau du bit de tous les styles qui seront autorisés à changer.</span><span class="sxs-lookup"><span data-stu-id="181ca-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="181ca-112"><span id="value"></span><span id="VALUE"></span>*ajoutée*</span><span class="sxs-lookup"><span data-stu-id="181ca-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="181ca-113">Nouveaux paramètres de style pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="181ca-113">New style settings for the window.</span></span> <span data-ttu-id="181ca-114">Spécifiez zéro pour ce paramètre pour désactiver tous les styles identifiés dans le masque.</span><span class="sxs-lookup"><span data-stu-id="181ca-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="181ca-115">Pour obtenir la liste des styles disponibles, consultez la fonction [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="181ca-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="181ca-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="181ca-116">Return Value</span></span>

<span data-ttu-id="181ca-117">Retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="181ca-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="181ca-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="181ca-118">Requirements</span></span>



| <span data-ttu-id="181ca-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="181ca-119">Requirement</span></span> | <span data-ttu-id="181ca-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="181ca-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="181ca-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="181ca-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181ca-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="181ca-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="181ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="181ca-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="181ca-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="181ca-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="181ca-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="181ca-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="181ca-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="181ca-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="181ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181ca-128">**MCIWndCreate**</span><span class="sxs-lookup"><span data-stu-id="181ca-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="181ca-129">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="181ca-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





