---
title: Message RB_SETPALETTE (commctrl. h)
description: Définit la palette actuelle du contrôle rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942457"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="576c9-104">\_Message SETPALETTE RB</span><span class="sxs-lookup"><span data-stu-id="576c9-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="576c9-105">Définit la palette actuelle du contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="576c9-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="576c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="576c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="576c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="576c9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="576c9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="576c9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="576c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="576c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="576c9-110">**HPALETTE** qui spécifie la nouvelle palette que le contrôle rebar utilisera.</span><span class="sxs-lookup"><span data-stu-id="576c9-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="576c9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="576c9-111">Return value</span></span>

<span data-ttu-id="576c9-112">Retourne un **HPALETTE** qui spécifie la palette précédente du contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="576c9-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="576c9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="576c9-113">Remarks</span></span>

<span data-ttu-id="576c9-114">Il incombe à l’application d’envoyer ce message de supprimer le **HPALETTE** transmis dans ce message (voir [**SupprimerObjet**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span><span class="sxs-lookup"><span data-stu-id="576c9-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="576c9-115">Le contrôle rebar ne supprime pas un **HPALETTE** défini avec ce message.</span><span class="sxs-lookup"><span data-stu-id="576c9-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="576c9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="576c9-116">Requirements</span></span>



| <span data-ttu-id="576c9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="576c9-117">Requirement</span></span> | <span data-ttu-id="576c9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="576c9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="576c9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="576c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="576c9-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="576c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="576c9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="576c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="576c9-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="576c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="576c9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="576c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="576c9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="576c9-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="576c9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="576c9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="576c9-126">**\_GETPALETTE RB**</span><span class="sxs-lookup"><span data-stu-id="576c9-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

