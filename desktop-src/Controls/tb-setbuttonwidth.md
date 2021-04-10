---
title: Message TB_SETBUTTONWIDTH (commctrl. h)
description: Définit les largeurs minimale et maximale des boutons dans le contrôle ToolBar.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103759"
---
# <a name="tb_setbuttonwidth-message"></a><span data-ttu-id="883c5-104">TO \_ SETBUTTONWIDTH message</span><span class="sxs-lookup"><span data-stu-id="883c5-104">TB\_SETBUTTONWIDTH message</span></span>

<span data-ttu-id="883c5-105">Définit les largeurs minimale et maximale des boutons dans le contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="883c5-105">Sets the minimum and maximum button widths in the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="883c5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="883c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="883c5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="883c5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="883c5-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="883c5-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="883c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="883c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="883c5-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la largeur minimale du bouton, en pixels.</span><span class="sxs-lookup"><span data-stu-id="883c5-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum button width, in pixels.</span></span> <span data-ttu-id="883c5-111">Les boutons de la barre d’outils ne seront jamais plus étroits que cette valeur.</span><span class="sxs-lookup"><span data-stu-id="883c5-111">Toolbar buttons will never be narrower than this value.</span></span>

<span data-ttu-id="883c5-112">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la largeur maximale du bouton, en pixels.</span><span class="sxs-lookup"><span data-stu-id="883c5-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum button width, in pixels.</span></span> <span data-ttu-id="883c5-113">Si le texte du bouton est trop grand, le contrôle l’affiche avec des points de suspension.</span><span class="sxs-lookup"><span data-stu-id="883c5-113">If button text is too wide, the control displays it with ellipsis points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="883c5-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="883c5-114">Return value</span></span>

<span data-ttu-id="883c5-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="883c5-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="883c5-116">Notes</span><span class="sxs-lookup"><span data-stu-id="883c5-116">Remarks</span></span>

<span data-ttu-id="883c5-117">Utilisez **to \_ SETBUTTONWIDTH** pour définir les largeurs maximales et minimales autorisées pour les boutons avant leur ajout.</span><span class="sxs-lookup"><span data-stu-id="883c5-117">Use **TB\_SETBUTTONWIDTH** to set the maximum and minimum allowed widths for buttons before they are added.</span></span> <span data-ttu-id="883c5-118">Utilisez [**to \_ SETBUTTONSIZE**](tb-setbuttonsize.md) pour définir la taille réelle des boutons.</span><span class="sxs-lookup"><span data-stu-id="883c5-118">Use [**TB\_SETBUTTONSIZE**](tb-setbuttonsize.md) to set the actual size of buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="883c5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="883c5-119">Requirements</span></span>



| <span data-ttu-id="883c5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="883c5-120">Requirement</span></span> | <span data-ttu-id="883c5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="883c5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="883c5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="883c5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="883c5-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="883c5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="883c5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="883c5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="883c5-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="883c5-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="883c5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="883c5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="883c5-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="883c5-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

