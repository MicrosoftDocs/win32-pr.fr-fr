---
title: Message LVM_ENABLEGROUPVIEW (commctrl. h)
description: Active ou désactive si les éléments d’un contrôle List View s’affichent en tant que groupe.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032364"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="b181a-104">\_Message ENABLEGROUPVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="b181a-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="b181a-105">Active ou désactive si les éléments d’un contrôle List View s’affichent en tant que groupe.</span><span class="sxs-lookup"><span data-stu-id="b181a-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="b181a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b181a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b181a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b181a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b181a-108">Valeur **booléenne** qui indique s’il faut activer un contrôle d’affichage de liste pour regrouper les éléments affichés.</span><span class="sxs-lookup"><span data-stu-id="b181a-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="b181a-109">Utilisez **true** pour activer le regroupement, **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="b181a-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="b181a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b181a-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b181a-111">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b181a-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b181a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b181a-112">Return value</span></span>

<span data-ttu-id="b181a-113">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b181a-113">Returns one of the following values.</span></span>



| <span data-ttu-id="b181a-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b181a-114">Return code</span></span>                                                                       | <span data-ttu-id="b181a-115">Description</span><span class="sxs-lookup"><span data-stu-id="b181a-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b181a-116"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="b181a-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="b181a-117">La possibilité d’afficher des éléments de vue liste en tant que groupe est déjà activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="b181a-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="b181a-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b181a-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="b181a-119">L’état du contrôle a été correctement modifié.</span><span class="sxs-lookup"><span data-stu-id="b181a-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="b181a-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="b181a-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="b181a-121">L'opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="b181a-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="b181a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b181a-122">Remarks</span></span>

<span data-ttu-id="b181a-123">**LVM \_ ENABLEGROUPVIEW** n’est pas pris en charge sous le style [**\_ OWNERDATA LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b181a-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="b181a-124">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="b181a-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b181a-125">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b181a-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b181a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b181a-126">Requirements</span></span>



| <span data-ttu-id="b181a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b181a-127">Requirement</span></span> | <span data-ttu-id="b181a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b181a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b181a-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b181a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b181a-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b181a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b181a-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b181a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b181a-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b181a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b181a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="b181a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b181a-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b181a-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





