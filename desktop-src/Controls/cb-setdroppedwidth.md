---
title: Message CB_SETDROPPEDWIDTH (winuser. h)
description: Une application envoie le \_ message CB SETDROPPEDWIDTH pour définir la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la liste \_ déroulante CBS ou le \_ style DropDownList SCC.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843561"
---
# <a name="cb_setdroppedwidth-message"></a><span data-ttu-id="f2834-104">\_Message SETDROPPEDWIDTH CB</span><span class="sxs-lookup"><span data-stu-id="f2834-104">CB\_SETDROPPEDWIDTH message</span></span>

<span data-ttu-id="f2834-105">Une application envoie le message **CB \_ SETDROPPEDWIDTH** pour définir la largeur minimale autorisée, en pixels, de la zone de liste d’une zone de liste déroulante avec la liste [**\_ déroulante CBS**](combo-box-styles.md) ou le style [**\_ DropDownList SCC**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f2834-105">An application sends the **CB\_SETDROPPEDWIDTH** message to set the minimum allowable width, in pixels, of the list box of a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2834-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2834-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2834-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2834-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2834-108">Largeur minimale autorisée de la zone de liste, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f2834-108">The minimum allowable width of the list box, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f2834-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2834-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f2834-110">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f2834-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2834-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2834-111">Return value</span></span>

<span data-ttu-id="f2834-112">Si le message est réussi, la valeur de retour est la nouvelle largeur de la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="f2834-112">If the message is successful, The return value is the new width of the list box.</span></span>

<span data-ttu-id="f2834-113">Si le message échoue, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f2834-113">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2834-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f2834-114">Remarks</span></span>

<span data-ttu-id="f2834-115">Par défaut, la largeur minimale autorisée de la zone de liste déroulante est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="f2834-115">By default, the minimum allowable width of the drop-down list box is zero.</span></span> <span data-ttu-id="f2834-116">La largeur de la zone de liste est la largeur minimale autorisée ou la largeur de zone de liste déroulante, selon la valeur la plus grande.</span><span class="sxs-lookup"><span data-stu-id="f2834-116">The width of the list box is either the minimum allowable width or the combo box width, whichever is larger.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2834-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2834-117">Requirements</span></span>



| <span data-ttu-id="f2834-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2834-118">Requirement</span></span> | <span data-ttu-id="f2834-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2834-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2834-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2834-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2834-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2834-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f2834-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2834-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2834-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2834-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f2834-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2834-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2834-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2834-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2834-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2834-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2834-127">**\_GETDROPPEDWIDTH CB**</span><span class="sxs-lookup"><span data-stu-id="f2834-127">**CB\_GETDROPPEDWIDTH**</span></span>](cb-getdroppedwidth.md)
</dt> </dl>

 

 





