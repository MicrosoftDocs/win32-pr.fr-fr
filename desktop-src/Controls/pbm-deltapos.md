---
title: Message PBM_DELTAPOS (commctrl. h)
description: Avance la position actuelle d’une barre de progression d’un incrément spécifié et redessine la barre pour refléter la nouvelle position.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033051"
---
# <a name="pbm_deltapos-message"></a><span data-ttu-id="f96ad-104">\_Message PBM DELTAPOS</span><span class="sxs-lookup"><span data-stu-id="f96ad-104">PBM\_DELTAPOS message</span></span>

<span data-ttu-id="f96ad-105">Avance la position actuelle d’une barre de progression d’un incrément spécifié et redessine la barre pour refléter la nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="f96ad-105">Advances the current position of a progress bar by a specified increment and redraws the bar to reflect the new position.</span></span>

## <a name="parameters"></a><span data-ttu-id="f96ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f96ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f96ad-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f96ad-108">Montant d’avance de la position.</span><span class="sxs-lookup"><span data-stu-id="f96ad-108">Amount to advance the position.</span></span>

</dd> <dt>

<span data-ttu-id="f96ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f96ad-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f96ad-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="f96ad-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96ad-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f96ad-111">Return value</span></span>

<span data-ttu-id="f96ad-112">Retourne la position précédente.</span><span class="sxs-lookup"><span data-stu-id="f96ad-112">Returns the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="f96ad-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f96ad-113">Remarks</span></span>

<span data-ttu-id="f96ad-114">Si l’incrément produit une valeur en dehors de la plage du contrôle, la position est définie sur la limite la plus proche.</span><span class="sxs-lookup"><span data-stu-id="f96ad-114">If the increment results in a value outside the range of the control, the position is set to the nearest boundary.</span></span>

<span data-ttu-id="f96ad-115">Le comportement de ce message n’est pas défini s’il est envoyé à un contrôle dont le style [**PBS est \_ défilant**](progress-bar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f96ad-115">The behavior of this message is undefined if it is sent to a control that has the [**PBS\_MARQUEE**](progress-bar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96ad-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f96ad-116">Requirements</span></span>



| <span data-ttu-id="f96ad-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f96ad-117">Requirement</span></span> | <span data-ttu-id="f96ad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f96ad-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f96ad-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f96ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f96ad-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f96ad-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f96ad-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f96ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f96ad-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f96ad-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f96ad-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f96ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f96ad-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f96ad-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





