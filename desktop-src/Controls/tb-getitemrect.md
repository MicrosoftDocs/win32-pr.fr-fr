---
title: Message TB_GETITEMRECT (commctrl. h)
description: Récupère le rectangle englobant d’un bouton dans une barre d’outils.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843990"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="2eb4e-104">TO \_ GETITEMRECT message</span><span class="sxs-lookup"><span data-stu-id="2eb4e-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="2eb4e-105">Récupère le rectangle englobant d’un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="2eb4e-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2eb4e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2eb4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb4e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2eb4e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eb4e-108">Index de base zéro du bouton pour lequel des informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="2eb4e-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="2eb4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eb4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eb4e-110">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui reçoit les coordonnées clientes du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="2eb4e-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb4e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2eb4e-111">Return value</span></span>

<span data-ttu-id="2eb4e-112">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2eb4e-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eb4e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2eb4e-113">Remarks</span></span>

<span data-ttu-id="2eb4e-114">Ce message ne récupère pas le rectangle englobant pour les boutons dont l’État est défini sur la valeur [**\_ masquée TBSTATE**](toolbar-button-states.md) .</span><span class="sxs-lookup"><span data-stu-id="2eb4e-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb4e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2eb4e-115">Requirements</span></span>



| <span data-ttu-id="2eb4e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2eb4e-116">Requirement</span></span> | <span data-ttu-id="2eb4e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2eb4e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb4e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eb4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb4e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2eb4e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eb4e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2eb4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb4e-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2eb4e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eb4e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2eb4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb4e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb4e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

