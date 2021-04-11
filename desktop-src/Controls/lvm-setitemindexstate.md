---
title: Message LVM_SETITEMINDEXSTATE (commctrl. h)
description: Définit l’état d’un élément de vue liste. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView SetItemIndexState.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032619"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="55d36-105">\_Message SETITEMINDEXSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="55d36-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="55d36-106">Définit l’état d’un élément de vue liste.</span><span class="sxs-lookup"><span data-stu-id="55d36-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="55d36-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .</span><span class="sxs-lookup"><span data-stu-id="55d36-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="55d36-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55d36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d36-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d36-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d36-110">Pointeur vers une structure [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="55d36-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="55d36-111">Le processus appelant est chargé d’allouer cette structure et de définir les membres.</span><span class="sxs-lookup"><span data-stu-id="55d36-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="55d36-112">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="55d36-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55d36-113">Pointeur vers une structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="55d36-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="55d36-114">Le processus appelant est chargé d’allouer de la mémoire pour la structure.</span><span class="sxs-lookup"><span data-stu-id="55d36-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="55d36-115">Définissez le membre d' **État** sur une ou plusieurs (combinaison d’opérations de bits) des indicateurs d' [État d’élément de liste](list-view-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="55d36-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="55d36-116">Définissez le membre **stateMask** de la structure pour indiquer les bits valides du membre d' **État** .</span><span class="sxs-lookup"><span data-stu-id="55d36-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="55d36-117">Pour plus d’informations, consultez le membre **stateMask** de la structure **LVITEM** .</span><span class="sxs-lookup"><span data-stu-id="55d36-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55d36-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55d36-118">Return value</span></span>

<span data-ttu-id="55d36-119">Retourne l’une des valeurs suivantes de type **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="55d36-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="55d36-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="55d36-120">Return code</span></span>                                                                                  | <span data-ttu-id="55d36-121">Description</span><span class="sxs-lookup"><span data-stu-id="55d36-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="55d36-122"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="55d36-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="55d36-123">Impossible de définir l’État.</span><span class="sxs-lookup"><span data-stu-id="55d36-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="55d36-124"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="55d36-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="55d36-125">Le contrôle List-View n’était pas prêt pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="55d36-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="55d36-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55d36-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="55d36-127">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="55d36-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="55d36-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55d36-128">Requirements</span></span>



| <span data-ttu-id="55d36-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55d36-129">Requirement</span></span> | <span data-ttu-id="55d36-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="55d36-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55d36-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55d36-131">Minimum supported client</span></span><br/> | <span data-ttu-id="55d36-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55d36-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55d36-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="55d36-133">Minimum supported server</span></span><br/> | <span data-ttu-id="55d36-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="55d36-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55d36-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="55d36-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="55d36-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55d36-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





