---
title: Message LVM_GETINSERTMARKRECT (commctrl. h)
description: Récupère le rectangle qui délimite le point d’insertion.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942653"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="c3dcf-104">\_Message GETINSERTMARKRECT LVM</span><span class="sxs-lookup"><span data-stu-id="c3dcf-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="c3dcf-105">Récupère le rectangle qui délimite le point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3dcf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3dcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3dcf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3dcf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c3dcf-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="c3dcf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3dcf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3dcf-110">Pointeur vers une structure <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> qui contient les coordonnées d’un rectangle qui délimite le point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3dcf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3dcf-111">Return value</span></span>

<span data-ttu-id="c3dcf-112">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-112">Returns one of the following values.</span></span>



| <span data-ttu-id="c3dcf-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c3dcf-113">Return code</span></span>                                                                      | <span data-ttu-id="c3dcf-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3dcf-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="c3dcf-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c3dcf-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c3dcf-116">Aucun point d’insertion trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="c3dcf-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c3dcf-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c3dcf-118">Point d’insertion trouvé.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="c3dcf-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c3dcf-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c3dcf-120">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="c3dcf-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c3dcf-121">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c3dcf-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3dcf-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3dcf-122">Requirements</span></span>



| <span data-ttu-id="c3dcf-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3dcf-123">Requirement</span></span> | <span data-ttu-id="c3dcf-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3dcf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dcf-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3dcf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c3dcf-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3dcf-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3dcf-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3dcf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c3dcf-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3dcf-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3dcf-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3dcf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3dcf-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3dcf-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

