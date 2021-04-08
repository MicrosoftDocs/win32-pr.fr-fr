---
title: Message CB_GETITEMHEIGHT (winuser. h)
description: Détermine la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843573"
---
# <a name="cb_getitemheight-message"></a><span data-ttu-id="9da4f-104">\_Message GETITEMHEIGHT CB</span><span class="sxs-lookup"><span data-stu-id="9da4f-104">CB\_GETITEMHEIGHT message</span></span>

<span data-ttu-id="9da4f-105">Détermine la hauteur des éléments de liste ou le champ de sélection dans une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="9da4f-105">Determines the height of list items or the selection field in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9da4f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9da4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9da4f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9da4f-108">Composant de zone de liste déroulante dont la hauteur doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="9da4f-108">The combo box component whose height is to be retrieved.</span></span> <span data-ttu-id="9da4f-109">Ce paramètre doit avoir la valeur-1 pour récupérer la hauteur du champ de sélection.</span><span class="sxs-lookup"><span data-stu-id="9da4f-109">This parameter must be -1 to retrieve the height of the selection field.</span></span> <span data-ttu-id="9da4f-110">Elle doit être égale à zéro pour récupérer la hauteur des éléments de liste, sauf si la zone de liste déroulante a le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9da4f-110">It must be zero to retrieve the height of list items, unless the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="9da4f-111">Dans ce cas, le paramètre *wParam* est l’index de base zéro d’un élément de liste spécifique.</span><span class="sxs-lookup"><span data-stu-id="9da4f-111">In that case, the *wParam* parameter is the zero-based index of a specific list item.</span></span>

</dd> <dt>

<span data-ttu-id="9da4f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9da4f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9da4f-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9da4f-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da4f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9da4f-114">Return value</span></span>

<span data-ttu-id="9da4f-115">La valeur de retour correspond à la hauteur, en pixels, des éléments de liste dans une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="9da4f-115">The return value is the height, in pixels, of the list items in a combo box.</span></span> <span data-ttu-id="9da4f-116">Si la zone de liste déroulante a le style [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) , il s’agit de la hauteur de l’élément spécifié par le paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9da4f-116">If the combo box has the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, it is the height of the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="9da4f-117">Si *wParam* a la valeur-1, la valeur de retour est la hauteur de la partie de contrôle d’édition (ou de texte statique) de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="9da4f-117">If *wParam* is -1, the return value is the height of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="9da4f-118">Si une erreur se produit, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="9da4f-118">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="9da4f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9da4f-119">Requirements</span></span>



| <span data-ttu-id="9da4f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9da4f-120">Requirement</span></span> | <span data-ttu-id="9da4f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9da4f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da4f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9da4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9da4f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9da4f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9da4f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9da4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9da4f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9da4f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9da4f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9da4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9da4f-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9da4f-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da4f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9da4f-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="9da4f-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="9da4f-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9da4f-130">**\_SETITEMHEIGHT CB**</span><span class="sxs-lookup"><span data-stu-id="9da4f-130">**CB\_SETITEMHEIGHT**</span></span>](cb-setitemheight.md)
</dt> <dt>

[<span data-ttu-id="9da4f-131">**\_MEASUREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="9da4f-131">**WM\_MEASUREITEM**</span></span>](wm-measureitem.md)
</dt> </dl>

 

 





