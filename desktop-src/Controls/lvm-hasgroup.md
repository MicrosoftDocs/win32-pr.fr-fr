---
title: Message LVM_HASGROUP (commctrl. h)
description: Détermine si le contrôle d’affichage de liste possède un groupe spécifié.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466498"
---
# <a name="lvm_hasgroup-message"></a><span data-ttu-id="59164-104">\_Message HASGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="59164-104">LVM\_HASGROUP message</span></span>

<span data-ttu-id="59164-105">Détermine si le contrôle d’affichage de liste possède un groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="59164-105">Determines whether the list-view control has a specified group.</span></span>

## <a name="parameters"></a><span data-ttu-id="59164-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59164-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59164-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59164-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="59164-108">ID du groupe.</span><span class="sxs-lookup"><span data-stu-id="59164-108">ID of the group.</span></span></dd> <dt>

<span data-ttu-id="59164-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59164-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="59164-110">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="59164-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59164-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59164-111">Return value</span></span>

<span data-ttu-id="59164-112">Retourne la **valeur true** si le contrôle d’affichage de liste possède le groupe spécifié, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="59164-112">Returns **TRUE** if the list-view control has the specified group, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="59164-113">Notes</span><span class="sxs-lookup"><span data-stu-id="59164-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59164-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="59164-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="59164-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="59164-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59164-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59164-116">Requirements</span></span>



| <span data-ttu-id="59164-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59164-117">Requirement</span></span> | <span data-ttu-id="59164-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="59164-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59164-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59164-119">Minimum supported client</span></span><br/> | <span data-ttu-id="59164-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59164-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59164-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59164-121">Minimum supported server</span></span><br/> | <span data-ttu-id="59164-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59164-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59164-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="59164-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="59164-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="59164-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





