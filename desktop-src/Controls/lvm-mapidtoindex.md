---
title: Message LVM_MAPIDTOINDEX (commctrl. h)
description: Mappe l’ID d’un élément à un index.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509936"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="b57fe-104">\_Message MAPIDTOINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="b57fe-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="b57fe-105">Mappe l’ID d’un élément à un index.</span><span class="sxs-lookup"><span data-stu-id="b57fe-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="b57fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b57fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b57fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b57fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b57fe-108">ID unique d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b57fe-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="b57fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b57fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b57fe-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="b57fe-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b57fe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b57fe-111">Return value</span></span>

<span data-ttu-id="b57fe-112">Retourne l’index le plus récent.</span><span class="sxs-lookup"><span data-stu-id="b57fe-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="b57fe-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b57fe-113">Remarks</span></span>

<span data-ttu-id="b57fe-114">Les contrôles List-View effectuent le suivi interne des éléments par index.</span><span class="sxs-lookup"><span data-stu-id="b57fe-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="b57fe-115">Cela peut présenter des problèmes, car les index peuvent changer pendant la durée de vie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b57fe-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="b57fe-116">Le contrôle List-View peut baliser un élément avec un ID lors de la création de l’élément.</span><span class="sxs-lookup"><span data-stu-id="b57fe-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="b57fe-117">Vous pouvez utiliser cet ID pour garantir l’unicité pendant la durée de vie du contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="b57fe-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="b57fe-118">Pour identifier un élément de manière unique, prenez l’index retourné à partir d’un appel tel que [**IComponent :: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) et appelez [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md).</span><span class="sxs-lookup"><span data-stu-id="b57fe-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="b57fe-119">La valeur de retour est un ID unique.</span><span class="sxs-lookup"><span data-stu-id="b57fe-119">The return value is a unique ID.</span></span>

<span data-ttu-id="b57fe-120">Si vous avez besoin de l’index d’un élément après la création d’un ID, vous pouvez appeler **LVM \_ MAPIDTOINDEX** avec l’ID unique et il retourne l’index le plus récent.</span><span class="sxs-lookup"><span data-stu-id="b57fe-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="b57fe-121">**LVM \_ MAPIDTOINDEX** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b57fe-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="b57fe-122">Dans un environnement multithread, l’index est garanti uniquement sur le thread qui héberge le contrôle List-View, et non sur les threads d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b57fe-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="b57fe-123">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="b57fe-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b57fe-124">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b57fe-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b57fe-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b57fe-125">Requirements</span></span>



| <span data-ttu-id="b57fe-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b57fe-126">Requirement</span></span> | <span data-ttu-id="b57fe-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b57fe-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b57fe-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b57fe-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b57fe-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b57fe-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b57fe-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b57fe-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b57fe-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b57fe-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b57fe-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b57fe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b57fe-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b57fe-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

