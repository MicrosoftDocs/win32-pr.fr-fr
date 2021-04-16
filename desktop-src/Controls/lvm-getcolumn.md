---
title: Message LVM_GETCOLUMN (commctrl. h)
description: Obtient les attributs d’une colonne d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetColumn.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464279"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="30e7f-105">\_Message GETCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="30e7f-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="30e7f-106">Obtient les attributs d’une colonne d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="30e7f-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="30e7f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .</span><span class="sxs-lookup"><span data-stu-id="30e7f-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="30e7f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30e7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30e7f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30e7f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e7f-110">Index de la colonne.</span><span class="sxs-lookup"><span data-stu-id="30e7f-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="30e7f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30e7f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30e7f-112">Pointeur vers une structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) qui spécifie les informations pour récupérer et recevoir des informations sur la colonne.</span><span class="sxs-lookup"><span data-stu-id="30e7f-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="30e7f-113">Le membre **Mask** spécifie les attributs de colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="30e7f-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="30e7f-114">Si le membre de **masque** spécifie la \_ valeur de texte LVCF, le membre **pszText** doit contenir l’adresse de la mémoire tampon qui reçoit le texte de l’élément et le membre **cchTextMax** doit spécifier la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="30e7f-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30e7f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30e7f-115">Return value</span></span>

<span data-ttu-id="30e7f-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="30e7f-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e7f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30e7f-117">Requirements</span></span>



| <span data-ttu-id="30e7f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30e7f-118">Requirement</span></span> | <span data-ttu-id="30e7f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="30e7f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30e7f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30e7f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30e7f-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30e7f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30e7f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30e7f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30e7f-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30e7f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30e7f-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="30e7f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30e7f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30e7f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





