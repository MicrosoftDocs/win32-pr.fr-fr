---
title: Message LM_GETITEM (commctrl. h)
description: Récupère les États et les attributs d’un élément.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102920"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="3234e-104">\_Message LM GETITEM</span><span class="sxs-lookup"><span data-stu-id="3234e-104">LM\_GETITEM message</span></span>

<span data-ttu-id="3234e-105">Récupère les États et les attributs d’un élément.</span><span class="sxs-lookup"><span data-stu-id="3234e-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="3234e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3234e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3234e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3234e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3234e-108">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3234e-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="3234e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3234e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3234e-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> à remplir avec des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="3234e-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3234e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3234e-111">Return value</span></span>

<span data-ttu-id="3234e-112">Retourne la **valeur true** si le message parvient à obtenir les valeurs et les attributs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3234e-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="3234e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3234e-113">Remarks</span></span>

<span data-ttu-id="3234e-114">Avec le message **LM \_ GETITEM** , les liens sont accessibles uniquement par le biais de l’index numérique renvoyé dans le membre **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="3234e-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="3234e-115">L’accès au lien via le nom d’ID renvoyé dans **szID** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3234e-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="3234e-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="3234e-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="3234e-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3234e-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3234e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3234e-118">Requirements</span></span>



| <span data-ttu-id="3234e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3234e-119">Requirement</span></span> | <span data-ttu-id="3234e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="3234e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3234e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3234e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3234e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3234e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3234e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3234e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3234e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3234e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3234e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3234e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3234e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3234e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





