---
title: Message EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtient le nombre de lignes dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104833"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="2fbd9-104">Message EM_GETFILELINECOUNT (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="2fbd9-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="2fbd9-105">Obtient le nombre de lignes dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fbd9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fbd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fbd9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fbd9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fbd9-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2fbd9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fbd9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fbd9-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fbd9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fbd9-111">Return value</span></span>

<span data-ttu-id="2fbd9-112">La valeur de retour est un entier spécifiant le nombre total de lignes de texte dans le contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="2fbd9-113">Si le contrôle n’a pas de texte, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="2fbd9-114">La valeur de retour ne sera jamais inférieure à 1.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fbd9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2fbd9-115">Remarks</span></span>

<span data-ttu-id="2fbd9-116">Le message **em \_ GETFILELINECOUNT** récupère le nombre total de lignes de texte, indépendamment de la façon dont les lignes sont affichées à l’écran, et pas seulement du nombre de lignes actuellement visibles.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="2fbd9-117">Le retour automatique à la ligne ne change pas le nombre de lignes renvoyées par ce message, car ce message fonctionne indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2fbd9-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fbd9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fbd9-118">Requirements</span></span>



| <span data-ttu-id="2fbd9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fbd9-119">Requirement</span></span> | <span data-ttu-id="2fbd9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fbd9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fbd9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fbd9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2fbd9-122">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fbd9-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2fbd9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fbd9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2fbd9-124">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2fbd9-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2fbd9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2fbd9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fbd9-126"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fbd9-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fbd9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fbd9-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="2fbd9-128">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2fbd9-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2fbd9-129">**\_GETFILELINE em**</span><span class="sxs-lookup"><span data-stu-id="2fbd9-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="2fbd9-130">**\_FILELINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="2fbd9-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="2fbd9-131">**Modifier \_ GetFileLineCount**</span><span class="sxs-lookup"><span data-stu-id="2fbd9-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





