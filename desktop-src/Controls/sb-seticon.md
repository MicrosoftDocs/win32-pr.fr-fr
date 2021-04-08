---
title: Message SB_SETICON (commctrl. h)
description: Définit l’icône d’un composant dans une barre d’État.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843997"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="2b8bd-104">\_Message SB SETICON</span><span class="sxs-lookup"><span data-stu-id="2b8bd-104">SB\_SETICON message</span></span>

<span data-ttu-id="2b8bd-105">Définit l’icône d’un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b8bd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b8bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b8bd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b8bd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8bd-108">Index de base zéro de la partie qui recevra l’icône.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="2b8bd-109">Si ce paramètre a la valeur-1, la barre d’État est supposée être une barre d’état simple.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="2b8bd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b8bd-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b8bd-111">Handle de l’icône à définir.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-111">Handle to the icon to be set.</span></span> <span data-ttu-id="2b8bd-112">Si cette valeur est **null**, l’icône est supprimée de la partie.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b8bd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b8bd-113">Return value</span></span>

<span data-ttu-id="2b8bd-114">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8bd-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2b8bd-115">Remarks</span></span>

<span data-ttu-id="2b8bd-116">La barre d’État ne détruit pas l’icône.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="2b8bd-117">Il incombe à l’application appelante d’effectuer le suivi et de détruire les icônes.</span><span class="sxs-lookup"><span data-stu-id="2b8bd-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8bd-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b8bd-118">Requirements</span></span>



| <span data-ttu-id="2b8bd-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b8bd-119">Requirement</span></span> | <span data-ttu-id="2b8bd-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b8bd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8bd-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b8bd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8bd-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b8bd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b8bd-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b8bd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8bd-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b8bd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b8bd-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b8bd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b8bd-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b8bd-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





