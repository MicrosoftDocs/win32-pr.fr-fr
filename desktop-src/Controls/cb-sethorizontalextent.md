---
title: Message CB_SETHORIZONTALEXTENT (winuser. h)
description: Une application envoie le \_ message CB SETHORIZONTALEXTENT pour définir la largeur, en pixels, par laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- CB_SETHORIZONTALEXTENT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465250"
---
# <a name="cb_sethorizontalextent-message"></a><span data-ttu-id="07774-104">\_Message SETHORIZONTALEXTENT CB</span><span class="sxs-lookup"><span data-stu-id="07774-104">CB\_SETHORIZONTALEXTENT message</span></span>

<span data-ttu-id="07774-105">Une application envoie le message **CB \_ SETHORIZONTALEXTENT** pour définir la largeur, en pixels, par laquelle une zone de liste peut faire défiler horizontalement (la largeur avec défilement).</span><span class="sxs-lookup"><span data-stu-id="07774-105">An application sends the **CB\_SETHORIZONTALEXTENT** message to set the width, in pixels, by which a list box can be scrolled horizontally (the scrollable width).</span></span> <span data-ttu-id="07774-106">Si la largeur de la zone de liste est inférieure à cette valeur, la barre de défilement horizontale fait défiler horizontalement les éléments de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="07774-106">If the width of the list box is smaller than this value, the horizontal scroll bar horizontally scrolls items in the list box.</span></span> <span data-ttu-id="07774-107">Si la largeur de la zone de liste est supérieure ou égale à cette valeur, la barre de défilement horizontale est masquée ou, si la zone de liste déroulante a le style [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) , désactivé.</span><span class="sxs-lookup"><span data-stu-id="07774-107">If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [**CBS\_DISABLENOSCROLL**](combo-box-styles.md) style, disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="07774-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07774-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07774-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07774-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07774-110">Spécifie la largeur de défilement de la zone de liste, en pixels.</span><span class="sxs-lookup"><span data-stu-id="07774-110">Specifies the scrollable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="07774-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07774-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07774-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="07774-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07774-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07774-113">Requirements</span></span>



| <span data-ttu-id="07774-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07774-114">Requirement</span></span> | <span data-ttu-id="07774-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="07774-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07774-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07774-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07774-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07774-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="07774-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07774-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07774-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07774-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07774-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="07774-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07774-121"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07774-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07774-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07774-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07774-123">**\_GETHORIZONTALEXTENT CB**</span><span class="sxs-lookup"><span data-stu-id="07774-123">**CB\_GETHORIZONTALEXTENT**</span></span>](cb-gethorizontalextent.md)
</dt> </dl>

 

 





