---
title: Message LVM_SORTGROUPS (commctrl. h)
description: Utilise une fonction de comparaison définie par l’application pour trier des groupes par ID au sein d’un contrôle List-View.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105460"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="65595-104">\_Message SORTGROUPS LVM</span><span class="sxs-lookup"><span data-stu-id="65595-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="65595-105">Utilise une fonction de comparaison définie par l’application pour trier des groupes par ID au sein d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="65595-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="65595-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65595-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65595-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="65595-108">Pointeur vers une fonction de comparaison définie par l’application, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span><span class="sxs-lookup"><span data-stu-id="65595-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="65595-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65595-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="65595-110">Pointeur void vers les informations définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="65595-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65595-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65595-111">Return value</span></span>

<span data-ttu-id="65595-112">Retourne 1 en cas de réussite, ou 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="65595-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65595-113">Notes</span><span class="sxs-lookup"><span data-stu-id="65595-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65595-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="65595-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="65595-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="65595-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65595-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65595-116">Requirements</span></span>



| <span data-ttu-id="65595-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65595-117">Requirement</span></span> | <span data-ttu-id="65595-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="65595-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65595-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65595-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65595-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65595-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65595-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65595-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65595-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65595-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65595-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="65595-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="65595-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65595-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65595-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65595-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65595-126">**LVGroupCompare**</span><span class="sxs-lookup"><span data-stu-id="65595-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

