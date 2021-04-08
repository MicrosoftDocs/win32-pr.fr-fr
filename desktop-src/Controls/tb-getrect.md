---
title: Message TB_GETRECT (commctrl. h)
description: Récupère le rectangle englobant d’un bouton de barre d’outils spécifié.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- TB_GETRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844370"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="da2a1-104">TO \_ GETRECT message</span><span class="sxs-lookup"><span data-stu-id="da2a1-104">TB\_GETRECT message</span></span>

<span data-ttu-id="da2a1-105">Récupère le rectangle englobant d’un bouton de barre d’outils spécifié.</span><span class="sxs-lookup"><span data-stu-id="da2a1-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="da2a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da2a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2a1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da2a1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da2a1-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="da2a1-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="da2a1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da2a1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da2a1-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="da2a1-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2a1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da2a1-111">Return value</span></span>

<span data-ttu-id="da2a1-112">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="da2a1-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="da2a1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="da2a1-113">Remarks</span></span>

<span data-ttu-id="da2a1-114">Ce message ne récupère pas le rectangle englobant pour les boutons dont l’État est défini sur la valeur [**\_ masquée TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="da2a1-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="da2a1-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da2a1-115">Requirements</span></span>



| <span data-ttu-id="da2a1-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da2a1-116">Requirement</span></span> | <span data-ttu-id="da2a1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="da2a1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da2a1-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da2a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da2a1-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="da2a1-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da2a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da2a1-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da2a1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da2a1-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="da2a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="da2a1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2a1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

