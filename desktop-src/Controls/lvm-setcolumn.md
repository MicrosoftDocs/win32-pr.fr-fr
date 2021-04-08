---
title: Message LVM_SETCOLUMN (commctrl. h)
description: Définit les attributs d’une colonne de vue de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SetColumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942164"
---
# <a name="lvm_setcolumn-message"></a><span data-ttu-id="e0d45-105">\_Message SETCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="e0d45-105">LVM\_SETCOLUMN message</span></span>

<span data-ttu-id="e0d45-106">Définit les attributs d’une colonne de vue de liste.</span><span class="sxs-lookup"><span data-stu-id="e0d45-106">Sets the attributes of a list-view column.</span></span> <span data-ttu-id="e0d45-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .</span><span class="sxs-lookup"><span data-stu-id="e0d45-107">You can send this message explicitly or by using the [**ListView\_SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0d45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0d45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0d45-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0d45-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d45-110">Index de la colonne.</span><span class="sxs-lookup"><span data-stu-id="e0d45-110">Index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="e0d45-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0d45-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d45-112">Pointeur vers une structure [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) qui contient les nouveaux attributs de colonne.</span><span class="sxs-lookup"><span data-stu-id="e0d45-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the new column attributes.</span></span> <span data-ttu-id="e0d45-113">Le membre **Mask** spécifie les attributs de colonne à définir.</span><span class="sxs-lookup"><span data-stu-id="e0d45-113">The **mask** member specifies which column attributes to set.</span></span> <span data-ttu-id="e0d45-114">Si le membre de **masque** spécifie la \_ valeur de texte LVCF, le membre **pszText** est l’adresse d’une chaîne terminée par le caractère null et le membre **cchTextMax** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e0d45-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0d45-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0d45-115">Return value</span></span>

<span data-ttu-id="e0d45-116">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e0d45-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d45-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0d45-117">Requirements</span></span>



| <span data-ttu-id="e0d45-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0d45-118">Requirement</span></span> | <span data-ttu-id="e0d45-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0d45-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d45-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0d45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d45-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0d45-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0d45-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0d45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d45-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0d45-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0d45-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0d45-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d45-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d45-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e0d45-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e0d45-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e0d45-127">**LVM \_ SETCOLUMNW** (Unicode) et **LVM \_ SETCOLUMNW** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e0d45-127">**LVM\_SETCOLUMNW** (Unicode) and **LVM\_SETCOLUMNW** (ANSI)</span></span><br/>               |



 

 





