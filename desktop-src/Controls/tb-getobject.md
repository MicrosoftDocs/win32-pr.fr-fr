---
title: Message TB_GETOBJECT (commctrl. h)
description: Récupère le IDropTarget pour un contrôle ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105055"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="0e24d-104">TO \_ GETOBJECT message</span><span class="sxs-lookup"><span data-stu-id="0e24d-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="0e24d-105">Récupère le [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pour un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="0e24d-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e24d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e24d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e24d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e24d-108">Identificateur de l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="0e24d-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="0e24d-109">Cette valeur doit pointer sur l' **IID \_ IDropTarget**.</span><span class="sxs-lookup"><span data-stu-id="0e24d-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="0e24d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e24d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e24d-111">Adresse qui reçoit le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="0e24d-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="0e24d-112">Si une erreur se produit, un pointeur **null** est placé dans cette adresse.</span><span class="sxs-lookup"><span data-stu-id="0e24d-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e24d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e24d-113">Return value</span></span>

<span data-ttu-id="0e24d-114">Retourne une valeur **HRESULT** indiquant la réussite ou l’échec de l’opération.</span><span class="sxs-lookup"><span data-stu-id="0e24d-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e24d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0e24d-115">Remarks</span></span>

<span data-ttu-id="0e24d-116">Le [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de la barre d’outils est utilisé par la barre d’outils lorsque les objets sont glissés ou déplacés dessus.</span><span class="sxs-lookup"><span data-stu-id="0e24d-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e24d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e24d-117">Requirements</span></span>



| <span data-ttu-id="0e24d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e24d-118">Requirement</span></span> | <span data-ttu-id="0e24d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e24d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e24d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e24d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e24d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e24d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e24d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e24d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e24d-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e24d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e24d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e24d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e24d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e24d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

