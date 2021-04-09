---
title: Message CB_SETCURSEL (winuser. h)
description: Une application envoie un \_ message CB SETCURSEL pour sélectionner une chaîne dans la liste d’une zone de liste déroulante.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032843"
---
# <a name="cb_setcursel-message"></a><span data-ttu-id="625e7-104">\_Message SETCURSEL CB</span><span class="sxs-lookup"><span data-stu-id="625e7-104">CB\_SETCURSEL message</span></span>

<span data-ttu-id="625e7-105">Une application envoie un message **CB \_ SETCURSEL** pour sélectionner une chaîne dans la liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="625e7-105">An application sends a **CB\_SETCURSEL** message to select a string in the list of a combo box.</span></span> <span data-ttu-id="625e7-106">Si nécessaire, la liste fait défiler la chaîne dans la vue.</span><span class="sxs-lookup"><span data-stu-id="625e7-106">If necessary, the list scrolls the string into view.</span></span> <span data-ttu-id="625e7-107">Le texte du contrôle d’édition de la zone de liste déroulante change pour refléter la nouvelle sélection, et toute sélection précédente dans la liste est supprimée.</span><span class="sxs-lookup"><span data-stu-id="625e7-107">The text in the edit control of the combo box changes to reflect the new selection, and any previous selection in the list is removed.</span></span>

## <a name="parameters"></a><span data-ttu-id="625e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="625e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="625e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="625e7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="625e7-110">Spécifie l’index de base zéro de la chaîne à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="625e7-110">Specifies the zero-based index of the string to select.</span></span> <span data-ttu-id="625e7-111">Si ce paramètre est défini sur-1, toute sélection en cours dans la liste est supprimée et le contrôle d’édition est effacé.</span><span class="sxs-lookup"><span data-stu-id="625e7-111">If this parameter is -1, any current selection in the list is removed and the edit control is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="625e7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="625e7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="625e7-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="625e7-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="625e7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="625e7-114">Return value</span></span>

<span data-ttu-id="625e7-115">Si le message est réussi, la valeur de retour est l’index de l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="625e7-115">If the message is successful, the return value is the index of the item selected.</span></span> <span data-ttu-id="625e7-116">Si *wParam* est supérieur au nombre d’éléments dans la liste ou si *wParam* a la valeur-1, la valeur de retour est CB \_ Err et la sélection est désactivée.</span><span class="sxs-lookup"><span data-stu-id="625e7-116">If *wParam* is greater than the number of items in the list or if *wParam* is -1, the return value is CB\_ERR and the selection is cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="625e7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="625e7-117">Requirements</span></span>



| <span data-ttu-id="625e7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="625e7-118">Requirement</span></span> | <span data-ttu-id="625e7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="625e7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="625e7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="625e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="625e7-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="625e7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="625e7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="625e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="625e7-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="625e7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="625e7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="625e7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="625e7-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="625e7-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="625e7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="625e7-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="625e7-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="625e7-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="625e7-128">**\_FindString CB**</span><span class="sxs-lookup"><span data-stu-id="625e7-128">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="625e7-129">**\_GETCURSEL CB**</span><span class="sxs-lookup"><span data-stu-id="625e7-129">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="625e7-130">**\_SELECTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="625e7-130">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> </dl>

 

 





