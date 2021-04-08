---
title: Message TCM_HIGHLIGHTITEM (commctrl. h)
description: Définit l’état de surbrillance d’un élément d’onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- TCM_HIGHLIGHTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844173"
---
# <a name="tcm_highlightitem-message"></a><span data-ttu-id="50d3f-105">\_Message HIGHLIGHTITEM TCM</span><span class="sxs-lookup"><span data-stu-id="50d3f-105">TCM\_HIGHLIGHTITEM message</span></span>

<span data-ttu-id="50d3f-106">Définit l’état de surbrillance d’un élément d’onglet.</span><span class="sxs-lookup"><span data-stu-id="50d3f-106">Sets the highlight state of a tab item.</span></span> <span data-ttu-id="50d3f-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .</span><span class="sxs-lookup"><span data-stu-id="50d3f-107">You can send this message explicitly or by using the [**TabCtrl\_HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="50d3f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50d3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d3f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50d3f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50d3f-110">Valeur **int** qui spécifie l’index de base zéro d’un élément de contrôle d’onglet.</span><span class="sxs-lookup"><span data-stu-id="50d3f-110">An **INT** value that specifies the zero-based index of a tab control item.</span></span>

</dd> <dt>

<span data-ttu-id="50d3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50d3f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50d3f-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **bool** spécifiant l’état de mise en surbrillance à définir.</span><span class="sxs-lookup"><span data-stu-id="50d3f-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** specifying the highlight state to be set.</span></span> <span data-ttu-id="50d3f-113">Si cette valeur est **true**, l’onglet est mis en surbrillance ; Si la **valeur est false**, l’onglet est défini sur son état par défaut.</span><span class="sxs-lookup"><span data-stu-id="50d3f-113">If this value is **TRUE**, the tab is highlighted; if **FALSE**, the tab is set to its default state.</span></span> <span data-ttu-id="50d3f-114">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="50d3f-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d3f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50d3f-115">Return value</span></span>

<span data-ttu-id="50d3f-116">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="50d3f-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d3f-117">Notes</span><span class="sxs-lookup"><span data-stu-id="50d3f-117">Remarks</span></span>

<span data-ttu-id="50d3f-118">Dans Comctl32.dll version 6,0, ce message n’a aucun effet visible lorsqu’un thème est actif.</span><span class="sxs-lookup"><span data-stu-id="50d3f-118">In Comctl32.dll version 6.0, this message has no visible effect when a theme is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="50d3f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50d3f-119">Requirements</span></span>



| <span data-ttu-id="50d3f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50d3f-120">Requirement</span></span> | <span data-ttu-id="50d3f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="50d3f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50d3f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d3f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50d3f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50d3f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50d3f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d3f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50d3f-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50d3f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50d3f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="50d3f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d3f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d3f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

