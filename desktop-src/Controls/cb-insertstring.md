---
title: Message CB_INSERTSTRING (winuser. h)
description: Insère une chaîne ou des données d’élément dans la liste d’une zone de liste déroulante. Contrairement au \_ message CB ADDSTRING, le \_ message CB INSERTSTRING n’entraîne pas le tri d’une liste avec le \_ style de tri CBS.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465263"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="2c02c-105">\_Message INSERTSTRING CB</span><span class="sxs-lookup"><span data-stu-id="2c02c-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="2c02c-106">Insère une chaîne ou des données d’élément dans la liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="2c02c-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="2c02c-107">Contrairement au message [**CB \_ ADDSTRING**](cb-addstring.md) , le message **CB \_ INSERTSTRING** n’entraîne pas le tri d’une liste avec le style de [**\_ Tri CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2c02c-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c02c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c02c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c02c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c02c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c02c-110">Index de base zéro de la position à laquelle insérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="2c02c-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="2c02c-111">Si ce paramètre a la valeur-1, la chaîne est ajoutée à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="2c02c-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="2c02c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c02c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c02c-113">Pointeur vers la chaîne terminée par le caractère null à insérer.</span><span class="sxs-lookup"><span data-stu-id="2c02c-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="2c02c-114">Si vous créez la zone de liste déroulante avec un style owner-drawn, mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la valeur du paramètre *lParam* est stockée au lieu de la chaîne dans laquelle elle pointe normalement.</span><span class="sxs-lookup"><span data-stu-id="2c02c-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c02c-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c02c-115">Return value</span></span>

<span data-ttu-id="2c02c-116">La valeur de retour est l’index de la position à laquelle la chaîne a été insérée.</span><span class="sxs-lookup"><span data-stu-id="2c02c-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="2c02c-117">Si une erreur se produit, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="2c02c-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="2c02c-118">Si l’espace disponible est insuffisant pour stocker la nouvelle chaîne, il s’agit de CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="2c02c-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="2c02c-119">Si la zone de liste déroulante a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous insérez une chaîne plus grande que la zone de liste modifiable, vous devez envoyer un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.</span><span class="sxs-lookup"><span data-stu-id="2c02c-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c02c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c02c-120">Requirements</span></span>



| <span data-ttu-id="2c02c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c02c-121">Requirement</span></span> | <span data-ttu-id="2c02c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c02c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c02c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c02c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2c02c-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c02c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c02c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c02c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2c02c-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c02c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2c02c-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c02c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c02c-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c02c-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c02c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c02c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c02c-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2c02c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2c02c-131">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="2c02c-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="2c02c-132">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="2c02c-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="2c02c-133">**\_Rép.**</span><span class="sxs-lookup"><span data-stu-id="2c02c-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 

