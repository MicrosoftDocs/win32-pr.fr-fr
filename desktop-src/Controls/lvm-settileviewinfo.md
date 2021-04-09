---
title: Message LVM_SETTILEVIEWINFO (commctrl. h)
description: Définit les informations qu’un contrôle List View utilise en mode mosaïque.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- LVM_SETTILEVIEWINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103352"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="ae604-104">\_Message SETTILEVIEWINFO LVM</span><span class="sxs-lookup"><span data-stu-id="ae604-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="ae604-105">Définit les informations qu’un contrôle List View utilise en mode mosaïque.</span><span class="sxs-lookup"><span data-stu-id="ae604-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae604-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae604-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae604-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae604-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ae604-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ae604-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ae604-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae604-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae604-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> qui contient les informations à définir.</span><span class="sxs-lookup"><span data-stu-id="ae604-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae604-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae604-111">Return value</span></span>

<span data-ttu-id="ae604-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ae604-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae604-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ae604-113">Remarks</span></span>

<span data-ttu-id="ae604-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="ae604-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ae604-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ae604-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae604-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae604-116">Requirements</span></span>



| <span data-ttu-id="ae604-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae604-117">Requirement</span></span> | <span data-ttu-id="ae604-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae604-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae604-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae604-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae604-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae604-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae604-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae604-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae604-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae604-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae604-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae604-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae604-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae604-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





