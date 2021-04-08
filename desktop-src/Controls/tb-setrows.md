---
title: Message TB_SETROWS (commctrl. h)
description: Définit le nombre de lignes de boutons dans une barre d’outils.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- TB_SETROWS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033264"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="369c4-104">TO \_ SETROWS message</span><span class="sxs-lookup"><span data-stu-id="369c4-104">TB\_SETROWS message</span></span>

<span data-ttu-id="369c4-105">Définit le nombre de lignes de boutons dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="369c4-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="369c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="369c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="369c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="369c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="369c4-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le nombre de lignes demandées.</span><span class="sxs-lookup"><span data-stu-id="369c4-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="369c4-109">Le nombre minimal de lignes est un, et le nombre maximal de lignes est égal au nombre de boutons dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="369c4-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="369c4-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est un **booléen** qui indique s’il faut créer plus de lignes que ce qui est demandé lorsque le système ne peut pas créer le nombre de lignes spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="369c4-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="369c4-111">Si la **valeur est true**, le système crée plus de lignes.</span><span class="sxs-lookup"><span data-stu-id="369c4-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="369c4-112">Si la **valeur est false**, le système crée moins de lignes.</span><span class="sxs-lookup"><span data-stu-id="369c4-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="369c4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="369c4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="369c4-114">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit le rectangle englobant de la barre d’outils une fois les lignes définies.</span><span class="sxs-lookup"><span data-stu-id="369c4-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="369c4-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="369c4-115">Return value</span></span>

<span data-ttu-id="369c4-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="369c4-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="369c4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="369c4-117">Remarks</span></span>

<span data-ttu-id="369c4-118">Étant donné que le système ne scinde pas les groupes de boutons lors de la définition du nombre de lignes, le nombre de lignes résultant peut différer du nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="369c4-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="369c4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="369c4-119">Requirements</span></span>



| <span data-ttu-id="369c4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="369c4-120">Requirement</span></span> | <span data-ttu-id="369c4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="369c4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="369c4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="369c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="369c4-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="369c4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="369c4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="369c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="369c4-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="369c4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="369c4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="369c4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="369c4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="369c4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

