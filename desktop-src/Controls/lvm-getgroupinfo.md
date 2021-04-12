---
title: Message LVM_GETGROUPINFO (commctrl. h)
description: Obtient les informations de groupe.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032693"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="36ff2-104">\_Message GETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="36ff2-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="36ff2-105">Obtient les informations de groupe.</span><span class="sxs-lookup"><span data-stu-id="36ff2-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="36ff2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36ff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ff2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36ff2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="36ff2-108">ID qui spécifie le groupe dont les informations sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="36ff2-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="36ff2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36ff2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="36ff2-110">Pointeur une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> qui reçoit les informations récupérées.</span><span class="sxs-lookup"><span data-stu-id="36ff2-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="36ff2-111">Définissez le membre **cbSize** de cette structure sur sizeof (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="36ff2-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ff2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36ff2-112">Return value</span></span>

<span data-ttu-id="36ff2-113">Retourne l’ID du groupe en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="36ff2-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ff2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="36ff2-114">Remarks</span></span>

<span data-ttu-id="36ff2-115">Avant de tenter de récupérer l’en-tête d’un groupe, assurez-vous d’abord que le groupe n’a pas le \_ style d’en-tête LBGS.</span><span class="sxs-lookup"><span data-stu-id="36ff2-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="36ff2-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="36ff2-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="36ff2-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36ff2-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="36ff2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36ff2-118">Requirements</span></span>



| <span data-ttu-id="36ff2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36ff2-119">Requirement</span></span> | <span data-ttu-id="36ff2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="36ff2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36ff2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36ff2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="36ff2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36ff2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36ff2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36ff2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="36ff2-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36ff2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36ff2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="36ff2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="36ff2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ff2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





