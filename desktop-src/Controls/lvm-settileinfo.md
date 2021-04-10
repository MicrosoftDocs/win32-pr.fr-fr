---
title: Message LVM_SETTILEINFO (commctrl. h)
description: Définit des informations pour une vignette existante d’un contrôle List-View.
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- LVM_SETTILEINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103353"
---
# <a name="lvm_settileinfo-message"></a><span data-ttu-id="a1e48-104">\_Message SETTILEINFO LVM</span><span class="sxs-lookup"><span data-stu-id="a1e48-104">LVM\_SETTILEINFO message</span></span>

<span data-ttu-id="a1e48-105">Définit des informations pour une vignette existante d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="a1e48-105">Sets information for an existing tile of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1e48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1e48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e48-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1e48-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a1e48-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a1e48-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a1e48-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1e48-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a1e48-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> qui contient les informations à définir.</span><span class="sxs-lookup"><span data-stu-id="a1e48-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e48-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a1e48-111">Return value</span></span>

<span data-ttu-id="a1e48-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1e48-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e48-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a1e48-113">Remarks</span></span>

<span data-ttu-id="a1e48-114">**LVM \_ SETTILEINFO** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a1e48-114">**LVM\_SETTILEINFO** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="a1e48-115">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="a1e48-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a1e48-116">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a1e48-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1e48-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1e48-117">Requirements</span></span>



| <span data-ttu-id="a1e48-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1e48-118">Requirement</span></span> | <span data-ttu-id="a1e48-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1e48-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e48-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1e48-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e48-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1e48-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1e48-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1e48-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e48-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1e48-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1e48-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1e48-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e48-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1e48-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





