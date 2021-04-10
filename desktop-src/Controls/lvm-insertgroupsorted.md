---
title: Message LVM_INSERTGROUPSORTED (commctrl. h)
description: Insère un groupe dans une liste ordonnée de groupes.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- LVM_INSERTGROUPSORTED les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844082"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="04d84-104">\_Message INSERTGROUPSORTED LVM</span><span class="sxs-lookup"><span data-stu-id="04d84-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="04d84-105">Insère un groupe dans une liste ordonnée de groupes.</span><span class="sxs-lookup"><span data-stu-id="04d84-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="04d84-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d84-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04d84-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="04d84-108">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> qui contient le groupe à insérer.</span><span class="sxs-lookup"><span data-stu-id="04d84-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="04d84-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04d84-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="04d84-110">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="04d84-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d84-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04d84-111">Return value</span></span>

<span data-ttu-id="04d84-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="04d84-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d84-113">Notes</span><span class="sxs-lookup"><span data-stu-id="04d84-113">Remarks</span></span>

<span data-ttu-id="04d84-114">Le classement de la liste est basé sur l’ID du groupe.</span><span class="sxs-lookup"><span data-stu-id="04d84-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="04d84-115">L’ordre est défini par la fonction de tri définie par l’application, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), qui est transmise dans la structure [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="04d84-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="04d84-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="04d84-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="04d84-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="04d84-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04d84-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04d84-118">Requirements</span></span>



| <span data-ttu-id="04d84-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04d84-119">Requirement</span></span> | <span data-ttu-id="04d84-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="04d84-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04d84-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04d84-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04d84-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04d84-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04d84-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04d84-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04d84-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04d84-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04d84-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="04d84-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d84-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d84-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d84-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04d84-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="04d84-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="04d84-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04d84-129">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="04d84-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="04d84-130">**LVINSERTGROUPSORTED**</span><span class="sxs-lookup"><span data-stu-id="04d84-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

