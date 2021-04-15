---
title: Message CB_SETEDITSEL (winuser. h)
description: Une application envoie un \_ message CB SETEDITSEL pour sélectionner des caractères dans le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 25a07341-a21c-42a9-a220-62650997757b
keywords:
- CB_SETEDITSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_SETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54e09697e266b4e0c4260104e90f454a5e3edfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465251"
---
# <a name="cb_seteditsel-message"></a><span data-ttu-id="6fe01-104">\_Message SETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="6fe01-104">CB\_SETEDITSEL message</span></span>

<span data-ttu-id="6fe01-105">Une application envoie un message **CB \_ SETEDITSEL** pour sélectionner des caractères dans le contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="6fe01-105">An application sends a **CB\_SETEDITSEL** message to select characters in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fe01-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fe01-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe01-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6fe01-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fe01-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe01-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe01-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* spécifie la position de départ.</span><span class="sxs-lookup"><span data-stu-id="6fe01-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* specifies the starting position.</span></span> <span data-ttu-id="6fe01-111">Si le **LOWORD** est-1, la sélection, le cas échéant, est supprimée.</span><span class="sxs-lookup"><span data-stu-id="6fe01-111">If the **LOWORD** is -1, the selection, if any, is removed.</span></span>

<span data-ttu-id="6fe01-112">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de *lParam* spécifie la position de fin.</span><span class="sxs-lookup"><span data-stu-id="6fe01-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of *lParam* specifies the ending position.</span></span> <span data-ttu-id="6fe01-113">Si **HIWORD** a la valeur-1, tout le texte de la position de départ jusqu’au dernier caractère dans le contrôle d’édition est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6fe01-113">If the **HIWORD** is -1, all text from the starting position to the last character in the edit control is selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe01-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fe01-114">Return value</span></span>

<span data-ttu-id="6fe01-115">Si le message est correctement exécuté, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="6fe01-115">If the message succeeds, the return value is **TRUE**.</span></span> <span data-ttu-id="6fe01-116">Si le message est envoyé à une zone de liste déroulante avec le style de [**\_ DropDownList SCC**](combo-box-styles.md) , il s’agit de CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6fe01-116">If the message is sent to a combo box with the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe01-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6fe01-117">Remarks</span></span>

<span data-ttu-id="6fe01-118">Les positions sont de base zéro.</span><span class="sxs-lookup"><span data-stu-id="6fe01-118">The positions are zero-based.</span></span> <span data-ttu-id="6fe01-119">Le premier caractère du contrôle d’édition est dans la position zéro.</span><span class="sxs-lookup"><span data-stu-id="6fe01-119">The first character of the edit control is in the zero position.</span></span> <span data-ttu-id="6fe01-120">Le premier caractère après le dernier caractère sélectionné se trouve à la position de fin.</span><span class="sxs-lookup"><span data-stu-id="6fe01-120">The first character after the last selected character is in the ending position.</span></span> <span data-ttu-id="6fe01-121">Par exemple, pour sélectionner les quatre premiers caractères du contrôle d’édition, utilisez une position de départ de 0 et une position de fin de 4.</span><span class="sxs-lookup"><span data-stu-id="6fe01-121">For example, to select the first four characters of the edit control, use a starting position of 0 and an ending position of 4.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe01-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fe01-122">Requirements</span></span>



| <span data-ttu-id="6fe01-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fe01-123">Requirement</span></span> | <span data-ttu-id="6fe01-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fe01-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe01-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe01-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe01-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6fe01-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe01-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe01-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fe01-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fe01-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fe01-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fe01-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe01-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe01-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fe01-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="6fe01-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6fe01-133">**\_GETEDITSEL CB**</span><span class="sxs-lookup"><span data-stu-id="6fe01-133">**CB\_GETEDITSEL**</span></span>](cb-geteditsel.md)
</dt> <dt>

<span data-ttu-id="6fe01-134">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="6fe01-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6fe01-135">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="6fe01-135">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

