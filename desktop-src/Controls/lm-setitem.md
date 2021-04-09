---
title: Message LM_SETITEM (commctrl. h)
description: Définit les États et les attributs d’un élément.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102916"
---
# <a name="lm_setitem-message"></a><span data-ttu-id="ca884-104">\_Message LM SETITEM</span><span class="sxs-lookup"><span data-stu-id="ca884-104">LM\_SETITEM message</span></span>

<span data-ttu-id="ca884-105">Définit les États et les attributs d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ca884-105">Sets the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca884-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca884-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca884-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ca884-108">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ca884-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="ca884-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca884-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ca884-110">Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> contenant les nouveaux États et attributs souhaités pour le lien.</span><span class="sxs-lookup"><span data-stu-id="ca884-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure containing the new states and attributes desired for the link.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca884-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca884-111">Return value</span></span>

<span data-ttu-id="ca884-112">Retourne la **valeur true** si le message parvient à la définition des valeurs et des attributs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ca884-112">Returns **TRUE** if the message succeeds in setting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca884-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ca884-113">Remarks</span></span>

<span data-ttu-id="ca884-114">Avec le message [**LM \_ GETITEM**](lm-getitem.md) , les liens sont accessibles uniquement par le biais de l’index numérique renvoyé dans le membre **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="ca884-114">With the [**LM\_GETITEM**](lm-getitem.md) message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="ca884-115">L’accès au lien via le nom d’ID renvoyé dans **szID** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ca884-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="ca884-116">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comctl32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="ca884-116">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="ca884-117">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ca884-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ca884-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca884-118">Requirements</span></span>



| <span data-ttu-id="ca884-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca884-119">Requirement</span></span> | <span data-ttu-id="ca884-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca884-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca884-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca884-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ca884-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca884-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca884-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca884-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ca884-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca884-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca884-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca884-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca884-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca884-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





