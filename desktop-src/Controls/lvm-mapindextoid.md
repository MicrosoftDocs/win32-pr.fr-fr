---
title: Message LVM_MAPINDEXTOID (commctrl. h)
description: Mappe l’index d’un élément à un ID unique.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464890"
---
# <a name="lvm_mapindextoid-message"></a><span data-ttu-id="faa41-104">\_Message MAPINDEXTOID LVM</span><span class="sxs-lookup"><span data-stu-id="faa41-104">LVM\_MAPINDEXTOID message</span></span>

<span data-ttu-id="faa41-105">Mappe l’index d’un élément à un ID unique.</span><span class="sxs-lookup"><span data-stu-id="faa41-105">Maps the index of an item to a unique ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="faa41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faa41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa41-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="faa41-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa41-108">Index d’un élément.</span><span class="sxs-lookup"><span data-stu-id="faa41-108">The index of an item.</span></span>

</dd> <dt>

<span data-ttu-id="faa41-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faa41-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa41-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="faa41-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa41-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faa41-111">Return value</span></span>

<span data-ttu-id="faa41-112">Retourne un ID unique.</span><span class="sxs-lookup"><span data-stu-id="faa41-112">Returns a unique ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa41-113">Notes</span><span class="sxs-lookup"><span data-stu-id="faa41-113">Remarks</span></span>

<span data-ttu-id="faa41-114">Les contrôles List-View effectuent le suivi interne des éléments par index.</span><span class="sxs-lookup"><span data-stu-id="faa41-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="faa41-115">Cela peut présenter des problèmes, car les index peuvent changer pendant la durée de vie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="faa41-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="faa41-116">Le contrôle List-View peut baliser un élément avec un ID lors de la création de l’élément.</span><span class="sxs-lookup"><span data-stu-id="faa41-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="faa41-117">Vous pouvez utiliser cet ID pour garantir l’unicité pendant la durée de vie du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="faa41-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="faa41-118">Pour identifier un élément de manière unique, prenez l’index retourné à partir d’un appel tel que [**IComponent :: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) et appelez **LVM \_ MAPINDEXTOID**.</span><span class="sxs-lookup"><span data-stu-id="faa41-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call **LVM\_MAPINDEXTOID**.</span></span> <span data-ttu-id="faa41-119">La valeur de retour est un ID unique.</span><span class="sxs-lookup"><span data-stu-id="faa41-119">The return value is a unique ID.</span></span>

> [!Note]  
> <span data-ttu-id="faa41-120">Dans un environnement multithread, l’index est garanti uniquement sur le thread qui héberge le contrôle List-View, et non sur les threads d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="faa41-120">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="faa41-121">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="faa41-121">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="faa41-122">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="faa41-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="faa41-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faa41-123">Requirements</span></span>



| <span data-ttu-id="faa41-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faa41-124">Requirement</span></span> | <span data-ttu-id="faa41-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="faa41-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="faa41-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="faa41-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faa41-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="faa41-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="faa41-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faa41-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="faa41-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="faa41-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa41-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa41-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

