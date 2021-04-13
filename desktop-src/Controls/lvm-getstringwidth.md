---
title: Message LVM_GETSTRINGWIDTH (commctrl. h)
description: Détermine la largeur d’une chaîne spécifiée à l’aide de la police actuelle du contrôle List-View spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetStringWidth.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509158"
---
# <a name="lvm_getstringwidth-message"></a><span data-ttu-id="79584-105">\_Message GETSTRINGWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="79584-105">LVM\_GETSTRINGWIDTH message</span></span>

<span data-ttu-id="79584-106">Détermine la largeur d’une chaîne spécifiée à l’aide de la police actuelle du contrôle List-View spécifié.</span><span class="sxs-lookup"><span data-stu-id="79584-106">Determines the width of a specified string using the specified list-view control's current font.</span></span> <span data-ttu-id="79584-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) .</span><span class="sxs-lookup"><span data-stu-id="79584-107">You can send this message explicitly or by using the [**ListView\_GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79584-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79584-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79584-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79584-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="79584-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="79584-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="79584-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79584-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79584-112">Pointeur vers une chaîne se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="79584-112">Pointer to a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79584-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79584-113">Return value</span></span>

<span data-ttu-id="79584-114">Retourne la largeur de la chaîne en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="79584-114">Returns the string width if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79584-115">Notes</span><span class="sxs-lookup"><span data-stu-id="79584-115">Remarks</span></span>

<span data-ttu-id="79584-116">Le \_ message GETSTRINGWIDTH LVM retourne la largeur exacte, en pixels, de la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="79584-116">The LVM\_GETSTRINGWIDTH message returns the exact width, in pixels, of the specified string.</span></span> <span data-ttu-id="79584-117">Si vous utilisez la largeur de chaîne retournée comme largeur de colonne dans le message [**\_ SETCOLUMNWIDTH LVM**](lvm-setcolumnwidth.md) , la chaîne sera tronquée.</span><span class="sxs-lookup"><span data-stu-id="79584-117">If you use the returned string width as the column width in the [**LVM\_SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) message, the string will be truncated.</span></span> <span data-ttu-id="79584-118">Pour récupérer la largeur de colonne qui peut contenir la chaîne sans la tronquer, vous devez ajouter un remplissage à la largeur de chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="79584-118">To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width.</span></span>

## <a name="requirements"></a><span data-ttu-id="79584-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79584-119">Requirements</span></span>



| <span data-ttu-id="79584-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79584-120">Requirement</span></span> | <span data-ttu-id="79584-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="79584-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79584-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79584-122">Minimum supported client</span></span><br/> | <span data-ttu-id="79584-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79584-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79584-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79584-124">Minimum supported server</span></span><br/> | <span data-ttu-id="79584-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79584-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79584-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="79584-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="79584-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79584-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="79584-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="79584-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="79584-129">**LVM \_ GETSTRINGWIDTHW** (Unicode) et **LVM \_ GETSTRINGWIDTHA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="79584-129">**LVM\_GETSTRINGWIDTHW** (Unicode) and **LVM\_GETSTRINGWIDTHA** (ANSI)</span></span><br/>     |



 

 





