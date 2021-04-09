---
title: Message TVM_GETLINECOLOR (commctrl. h)
description: Le \_ message TVM GETLINECOLOR obtient la couleur de la ligne active.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- TVM_GETLINECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033009"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="dc0b4-104">TVM \_ GETLINECOLOR message</span><span class="sxs-lookup"><span data-stu-id="dc0b4-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="dc0b4-105">Le message **TVM \_ GETLINECOLOR** obtient la couleur de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc0b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc0b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc0b4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dc0b4-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dc0b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc0b4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dc0b4-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0b4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc0b4-111">Return value</span></span>

<span data-ttu-id="dc0b4-112">Retourne la couleur de la ligne active ou la \_ valeur CLR par défaut si aucune valeur n’a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc0b4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="dc0b4-113">Remarks</span></span>

<span data-ttu-id="dc0b4-114">Ce message récupère uniquement les couleurs de ligne.</span><span class="sxs-lookup"><span data-stu-id="dc0b4-114">This message only retrieves line colors.</span></span> <span data-ttu-id="dc0b4-115">Pour récupérer les couleurs de' + 'et'-'à l’intérieur des boutons, utilisez le message [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="dc0b4-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0b4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc0b4-116">Requirements</span></span>



| <span data-ttu-id="dc0b4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc0b4-117">Requirement</span></span> | <span data-ttu-id="dc0b4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc0b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0b4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc0b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dc0b4-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc0b4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc0b4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc0b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dc0b4-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc0b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc0b4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc0b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc0b4-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc0b4-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0b4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc0b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0b4-126">**TVM \_ SETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="dc0b4-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





