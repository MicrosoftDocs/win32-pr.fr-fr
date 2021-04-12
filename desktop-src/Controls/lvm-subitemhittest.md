---
title: Message LVM_SUBITEMHITTEST (commctrl. h)
description: Détermine l’élément de vue de liste ou le sous-élément qui se trouve à une position donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView SubItemHitTest.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464407"
---
# <a name="lvm_subitemhittest-message"></a><span data-ttu-id="0ce23-105">\_Message SUBITEMHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="0ce23-105">LVM\_SUBITEMHITTEST message</span></span>

<span data-ttu-id="0ce23-106">Détermine l’élément de vue de liste ou le sous-élément qui se trouve à une position donnée.</span><span class="sxs-lookup"><span data-stu-id="0ce23-106">Determines which list-view item or subitem is at a given position.</span></span> <span data-ttu-id="0ce23-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .</span><span class="sxs-lookup"><span data-stu-id="0ce23-107">You can send this message explicitly or by using the [**ListView\_SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0ce23-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ce23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ce23-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ce23-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0ce23-110">Doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="0ce23-110">Must be 0.</span></span> <span data-ttu-id="0ce23-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="0ce23-111">**Windows Vista.**</span></span> <span data-ttu-id="0ce23-112">Doit avoir la valeur-1 si le membre **iGroup** de *lParam* doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="0ce23-112">Should be -1 if the **iGroup** member of *lParam* is to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="0ce23-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ce23-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ce23-114">Pointeur vers une structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="0ce23-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure.</span></span> <span data-ttu-id="0ce23-115">La structure de [**points**](/previous-versions//dd162805(v=vs.85)) dans **LVHITTESTINFO** doit être définie sur les coordonnées clientes à tester.</span><span class="sxs-lookup"><span data-stu-id="0ce23-115">The [**POINT**](/previous-versions//dd162805(v=vs.85)) structure within **LVHITTESTINFO** should be set to the client coordinates to be hit-tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ce23-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ce23-116">Return value</span></span>

<span data-ttu-id="0ce23-117">Retourne l’index de l’élément ou du sous-élément testé, le cas échéant, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0ce23-117">Returns the index of the item or subitem tested, if any, or -1 otherwise.</span></span> <span data-ttu-id="0ce23-118">Si un élément ou un sous-élément se trouve aux coordonnées données, les champs de la structure [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) seront remplis avec les informations de correspondance applicables.</span><span class="sxs-lookup"><span data-stu-id="0ce23-118">If an item or subitem is at the given coordinates, the fields of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure will be filled with the applicable hit information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce23-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ce23-119">Requirements</span></span>



| <span data-ttu-id="0ce23-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ce23-120">Requirement</span></span> | <span data-ttu-id="0ce23-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ce23-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce23-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ce23-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce23-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ce23-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ce23-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ce23-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce23-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ce23-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ce23-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ce23-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ce23-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ce23-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

