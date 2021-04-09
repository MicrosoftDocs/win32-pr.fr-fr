---
title: Message CB_ADDSTRING (winuser. h)
description: Ajoute une chaîne à la zone de liste d’une zone de liste déroulante. Si la zone de liste déroulante n’a pas le \_ style de tri CBS, la chaîne est ajoutée à la fin de la liste. Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- CB_ADDSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942669"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="ab9d8-106">\_Message CB ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="ab9d8-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="ab9d8-107">Ajoute une chaîne à la zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="ab9d8-108">Si la zone de liste déroulante n’a pas le style de [**\_ Tri CBS**](combo-box-styles.md) , la chaîne est ajoutée à la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="ab9d8-109">Dans le cas contraire, la chaîne est insérée dans la liste et la liste est triée.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab9d8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab9d8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9d8-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab9d8-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab9d8-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ab9d8-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab9d8-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab9d8-114">Pointeur **LPCTSTR** vers la chaîne terminée par le caractère null à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="ab9d8-115">Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la valeur du paramètre *lParam* est stockée en tant que données d’élément et non pas en tant que chaîne vers laquelle pointe.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="ab9d8-116">Les données d’élément peuvent être récupérées ou modifiées en envoyant le message [**CB \_ GETITEMDATA**](cb-getitemdata.md) ou [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ab9d8-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9d8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab9d8-117">Return value</span></span>

<span data-ttu-id="ab9d8-118">La valeur de retour est l’index de base zéro de la chaîne dans la zone de liste de la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="ab9d8-119">Si une erreur se produit, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="ab9d8-120">Si l’espace disponible est insuffisant pour stocker la nouvelle chaîne, il s’agit de CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9d8-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ab9d8-121">Remarks</span></span>

<span data-ttu-id="ab9d8-122">Si vous créez une zone de liste déroulante owner-drawn avec le style de [**\_ Tri CBS**](combo-box-styles.md) mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , le message [**WM \_ COMPAREITEM**](wm-compareitem.md) est envoyé une ou plusieurs fois au propriétaire de la zone de liste déroulante afin que le nouvel élément puisse être placé correctement dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="ab9d8-123">Pour insérer une chaîne à un emplacement spécifique de la liste, utilisez le message [**CB \_ INSERTSTRING**](cb-insertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="ab9d8-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="ab9d8-124">Si la zone de liste déroulante a le style [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) et que vous ajoutez une chaîne plus grande que la zone de liste déroulante, envoyez un message [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) pour vous assurer que la barre de défilement horizontale s’affiche.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="ab9d8-125">**Comclt32.dll version 5,0 ou ultérieure :** Si les [**\_ majuscules**](combo-box-styles.md) CBS ou les majuscules CBS sont définies, la version Unicode de **CB \_ ADDSTRING** modifie la chaîne. [**\_**](combo-box-styles.md)</span><span class="sxs-lookup"><span data-stu-id="ab9d8-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="ab9d8-126">En cas d’utilisation de la mémoire globale en lecture seule, cela provoque l’échec de l’application.</span><span class="sxs-lookup"><span data-stu-id="ab9d8-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab9d8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab9d8-127">Requirements</span></span>



| <span data-ttu-id="ab9d8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab9d8-128">Requirement</span></span> | <span data-ttu-id="ab9d8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab9d8-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9d8-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab9d8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ab9d8-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab9d8-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab9d8-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab9d8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ab9d8-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab9d8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab9d8-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab9d8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab9d8-135"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab9d8-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab9d8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab9d8-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab9d8-137">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ab9d8-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab9d8-138">**\_Rép.**</span><span class="sxs-lookup"><span data-stu-id="ab9d8-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="ab9d8-139">**\_INSERTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="ab9d8-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="ab9d8-140">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="ab9d8-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="ab9d8-141">**\_COMPAREITEM WM**</span><span class="sxs-lookup"><span data-stu-id="ab9d8-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

