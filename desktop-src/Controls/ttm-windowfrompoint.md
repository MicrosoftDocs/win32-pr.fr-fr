---
title: Message TTM_WINDOWFROMPOINT (commctrl. h)
description: Permet à une procédure de sous-classe de faire en sorte qu’une info-bulle affiche du texte pour une fenêtre autre que celle située sous le curseur de la souris.
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742260"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="7db61-104">\_Message atténuation WINDOWFROMPOINT</span><span class="sxs-lookup"><span data-stu-id="7db61-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="7db61-105">Permet à une procédure de sous-classe de faire en sorte qu’une info-bulle affiche du texte pour une fenêtre autre que celle située sous le curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="7db61-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="7db61-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7db61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db61-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7db61-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7db61-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7db61-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7db61-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7db61-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7db61-110">Pointeur vers une structure [**point**](/previous-versions//dd162805(v=vs.85)) qui définit le point à vérifier.</span><span class="sxs-lookup"><span data-stu-id="7db61-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7db61-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7db61-111">Return value</span></span>

<span data-ttu-id="7db61-112">La valeur de retour est le handle de la fenêtre qui contient le point, ou **null** si aucune fenêtre n’existe au point spécifié.</span><span class="sxs-lookup"><span data-stu-id="7db61-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="7db61-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7db61-113">Remarks</span></span>

<span data-ttu-id="7db61-114">Ce message est destiné à être traité par une application qui sous-classe une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="7db61-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="7db61-115">Elle n’est pas destinée à être envoyée par une application.</span><span class="sxs-lookup"><span data-stu-id="7db61-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="7db61-116">Une info-bulle envoie ce message à lui-même avant d’afficher le texte d’une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7db61-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="7db61-117">En modifiant les coordonnées du point spécifié par *lParam*, la procédure de sous-classe peut faire en sorte que l’info-bulle affiche du texte pour une fenêtre autre que celle située sous le curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="7db61-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db61-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7db61-118">Requirements</span></span>



| <span data-ttu-id="7db61-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7db61-119">Requirement</span></span> | <span data-ttu-id="7db61-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7db61-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7db61-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7db61-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7db61-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7db61-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7db61-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7db61-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7db61-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7db61-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7db61-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7db61-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7db61-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7db61-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

