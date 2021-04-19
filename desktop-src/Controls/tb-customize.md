---
title: Message TB_CUSTOMIZE (commctrl. h)
description: Affiche la boîte de dialogue Personnaliser la barre d’outils.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509758"
---
# <a name="tb_customize-message"></a><span data-ttu-id="5b5f9-104">TO \_ personnaliser le message</span><span class="sxs-lookup"><span data-stu-id="5b5f9-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="5b5f9-105">Affiche la boîte de dialogue **personnaliser la barre d’outils** .</span><span class="sxs-lookup"><span data-stu-id="5b5f9-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b5f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b5f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b5f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b5f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b5f9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5b5f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b5f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b5f9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b5f9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b5f9-111">Return value</span></span>

<span data-ttu-id="5b5f9-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b5f9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5b5f9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5b5f9-114">La barre d’outils doit gérer les notifications [TBN \_ QUERYINSERT](tbn-queryinsert.md) et [TBN \_ QUERYDELETE](tbn-querydelete.md) pour que la boîte de dialogue **personnaliser la barre d’outils** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="5b5f9-115">Si la barre d’outils ne gère pas ces notifications, la **\_ personnalisation to** n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="5b5f9-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5b5f9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b5f9-116">Requirements</span></span>



| <span data-ttu-id="5b5f9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b5f9-117">Requirement</span></span> | <span data-ttu-id="5b5f9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b5f9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5f9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5f9-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b5f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b5f9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b5f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5f9-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b5f9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b5f9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b5f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5f9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5f9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





