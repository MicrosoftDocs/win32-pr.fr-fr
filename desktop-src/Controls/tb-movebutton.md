---
title: Message TB_MOVEBUTTON (commctrl. h)
description: Déplace un bouton d’un index vers un autre.
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- TB_MOVEBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_MOVEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dac4cd303e895998b12e710910432ba2c38b230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105046"
---
# <a name="tb_movebutton-message"></a><span data-ttu-id="e7367-104">TO \_ MOVEBUTTON message</span><span class="sxs-lookup"><span data-stu-id="e7367-104">TB\_MOVEBUTTON message</span></span>

<span data-ttu-id="e7367-105">Déplace un bouton d’un index vers un autre.</span><span class="sxs-lookup"><span data-stu-id="e7367-105">Moves a button from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7367-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7367-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7367-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7367-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7367-108">Index de base zéro du bouton à déplacer.</span><span class="sxs-lookup"><span data-stu-id="e7367-108">Zero-based index of the button to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="e7367-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7367-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7367-110">Index de base zéro où le bouton sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="e7367-110">Zero-based index where the button will be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7367-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7367-111">Return value</span></span>

<span data-ttu-id="e7367-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e7367-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7367-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7367-113">Requirements</span></span>



| <span data-ttu-id="e7367-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7367-114">Requirement</span></span> | <span data-ttu-id="e7367-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7367-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7367-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7367-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7367-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7367-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7367-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7367-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7367-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7367-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7367-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7367-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7367-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7367-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7367-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7367-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7367-123">**TO \_ SETANCHORHIGHLIGHT**</span><span class="sxs-lookup"><span data-stu-id="e7367-123">**TB\_SETANCHORHIGHLIGHT**</span></span>](tb-setanchorhighlight.md)
</dt> </dl>

 

 





