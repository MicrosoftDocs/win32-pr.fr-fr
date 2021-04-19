---
title: Message CB_SETITEMHEIGHT (winuser. h)
description: Une application envoie un \_ message CB SETITEMHEIGHT pour définir la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510169"
---
# <a name="cb_setitemheight-message"></a><span data-ttu-id="caff4-104">\_Message SETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="caff4-104">CB\_SETITEMHEIGHT message</span></span>

<span data-ttu-id="caff4-105">Une application envoie un message **CB \_ SETITEMHEIGHT** pour définir la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="caff4-105">An application sends a **CB\_SETITEMHEIGHT** message to set the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="caff4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caff4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caff4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="caff4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caff4-108">Spécifie le composant de la zone de liste déroulante pour laquelle la hauteur doit être définie.</span><span class="sxs-lookup"><span data-stu-id="caff4-108">Specifies the component of the combo box for which to set the height.</span></span>

<span data-ttu-id="caff4-109">Ce paramètre doit avoir la valeur 1 pour définir la hauteur du champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="caff4-109">This parameter must be  1 to set the height of the selection field.</span></span> <span data-ttu-id="caff4-110">Elle doit être égale à zéro pour définir la hauteur des éléments de liste, sauf si la zone de liste déroulante a le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="caff4-110">It must be zero to set the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="caff4-111">Dans ce cas, le paramètre *wParam* est l’index de base zéro d’un élément de liste spécifique.</span><span class="sxs-lookup"><span data-stu-id="caff4-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="caff4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="caff4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="caff4-113">Spécifie la hauteur, en pixels, du composant de zone de liste déroulante identifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="caff4-113">Specifies the height, in pixels, of the combo box component identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caff4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="caff4-114">Return value</span></span>

<span data-ttu-id="caff4-115">Si l’index ou la hauteur n’est pas valide, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="caff4-115">If the index or height is invalid, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="caff4-116">Notes</span><span class="sxs-lookup"><span data-stu-id="caff4-116">Remarks</span></span>

<span data-ttu-id="caff4-117">La hauteur du champ de sélection dans une zone de liste déroulante est définie indépendamment de la hauteur des éléments de la liste.</span><span class="sxs-lookup"><span data-stu-id="caff4-117">The selection field height in a combo box is set independently of the height of the list items.</span></span> <span data-ttu-id="caff4-118">Une application doit s’assurer que la hauteur du champ de sélection n’est pas inférieure à la hauteur d’un élément de liste particulier.</span><span class="sxs-lookup"><span data-stu-id="caff4-118">An application must ensure that the height of the selection field is not smaller than the height of a particular list item.</span></span>

## <a name="requirements"></a><span data-ttu-id="caff4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caff4-119">Requirements</span></span>



| <span data-ttu-id="caff4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caff4-120">Requirement</span></span> | <span data-ttu-id="caff4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="caff4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caff4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caff4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="caff4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caff4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="caff4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caff4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="caff4-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caff4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="caff4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="caff4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="caff4-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="caff4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caff4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caff4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="caff4-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="caff4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="caff4-130">**\_GETITEMHEIGHT CB**</span><span class="sxs-lookup"><span data-stu-id="caff4-130">**CB\_GETITEMHEIGHT**</span></span>](cb-getitemheight.md)
</dt> <dt>

[<span data-ttu-id="caff4-131">**\_MEASUREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="caff4-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





