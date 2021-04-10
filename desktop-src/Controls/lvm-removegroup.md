---
title: Message LVM_REMOVEGROUP (commctrl. h)
description: Supprime un groupe d’un contrôle List-View.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa631593e791f90c76a9f74aa1d967d9678540f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942381"
---
# <a name="lvm_removegroup-message"></a><span data-ttu-id="c5657-104">\_Message REMOVEGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="c5657-104">LVM\_REMOVEGROUP message</span></span>

<span data-ttu-id="c5657-105">Supprime un groupe d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="c5657-105">Removes a group from a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5657-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5657-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5657-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5657-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c5657-108">ID qui spécifie le groupe à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c5657-108">ID that specifies the group to remove.</span></span></dd> <dt>

<span data-ttu-id="c5657-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5657-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5657-110">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c5657-110">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5657-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5657-111">Return value</span></span>

<span data-ttu-id="c5657-112">Retourne l’index du groupe en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c5657-112">Returns the index of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5657-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c5657-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c5657-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c5657-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c5657-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c5657-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c5657-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5657-116">Requirements</span></span>



| <span data-ttu-id="c5657-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5657-117">Requirement</span></span> | <span data-ttu-id="c5657-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5657-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5657-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5657-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c5657-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5657-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5657-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5657-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c5657-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5657-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5657-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5657-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5657-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5657-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





