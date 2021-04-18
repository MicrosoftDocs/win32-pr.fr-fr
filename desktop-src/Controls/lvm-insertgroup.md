---
title: Message LVM_INSERTGROUP (commctrl. h)
description: Insère un groupe dans un contrôle List-View.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- LVM_INSERTGROUP les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511962"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="11ff7-104">\_Message INSERTGROUP LVM</span><span class="sxs-lookup"><span data-stu-id="11ff7-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="11ff7-105">Insère un groupe dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="11ff7-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="11ff7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11ff7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ff7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11ff7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="11ff7-108">Index où le groupe doit être ajouté.</span><span class="sxs-lookup"><span data-stu-id="11ff7-108">Index where the group is to be added.</span></span> <span data-ttu-id="11ff7-109">S’il s’agit de-1, le groupe est ajouté à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="11ff7-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="11ff7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11ff7-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="11ff7-111">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> qui contient le groupe à ajouter.</span><span class="sxs-lookup"><span data-stu-id="11ff7-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ff7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11ff7-112">Return value</span></span>

<span data-ttu-id="11ff7-113">Retourne l’index de l’élément auquel le groupe a été ajouté, ou-1 si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="11ff7-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ff7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="11ff7-114">Remarks</span></span>

<span data-ttu-id="11ff7-115">Pour activer le mode groupe, appelez [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) ou [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span><span class="sxs-lookup"><span data-stu-id="11ff7-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="11ff7-116">Un groupe ne peut pas être inséré dans un contrôle d’affichage de liste vide.</span><span class="sxs-lookup"><span data-stu-id="11ff7-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="11ff7-117">Veillez à définir le **iGroupId** dans le ou les éléments auxquels le groupe a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="11ff7-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="11ff7-118">Sinon, après le traitement du message [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) avec **true** , le contrôle ListView n’affichera aucun élément.</span><span class="sxs-lookup"><span data-stu-id="11ff7-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="11ff7-119">Pour utiliser ce message, vous devez fournir un manifeste spécifiant la version 6,0 de Comclt32.</span><span class="sxs-lookup"><span data-stu-id="11ff7-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="11ff7-120">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11ff7-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11ff7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11ff7-121">Requirements</span></span>



| <span data-ttu-id="11ff7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11ff7-122">Requirement</span></span> | <span data-ttu-id="11ff7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="11ff7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11ff7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11ff7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="11ff7-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11ff7-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11ff7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11ff7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="11ff7-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11ff7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11ff7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="11ff7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="11ff7-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="11ff7-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





