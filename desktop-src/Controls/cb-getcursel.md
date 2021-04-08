---
title: Message CB_GETCURSEL (winuser. h)
description: Une application envoie un \_ message CB GETCURSEL pour récupérer l’index de l’élément actuellement sélectionné, le cas échéant, dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844498"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="724b8-104">\_Message GETCURSEL CB</span><span class="sxs-lookup"><span data-stu-id="724b8-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="724b8-105">Une application envoie un message **CB \_ GETCURSEL** pour récupérer l’index de l’élément actuellement sélectionné, le cas échéant, dans la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="724b8-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="724b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="724b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="724b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="724b8-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="724b8-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="724b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="724b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="724b8-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="724b8-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724b8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="724b8-111">Return value</span></span>

<span data-ttu-id="724b8-112">La valeur de retour est l’index de base zéro de l’élément actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="724b8-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="724b8-113">Si aucun élément n’est sélectionné, il s’agit de CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="724b8-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="724b8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="724b8-114">Requirements</span></span>



| <span data-ttu-id="724b8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="724b8-115">Requirement</span></span> | <span data-ttu-id="724b8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="724b8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="724b8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="724b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="724b8-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="724b8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="724b8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="724b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="724b8-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="724b8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="724b8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="724b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="724b8-122"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="724b8-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724b8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="724b8-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="724b8-124">**Référence**</span><span class="sxs-lookup"><span data-stu-id="724b8-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="724b8-125">**\_SELECTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="724b8-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="724b8-126">**\_SETCURSEL CB**</span><span class="sxs-lookup"><span data-stu-id="724b8-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





