---
title: Message PBM_SETBARCOLOR (commctrl. h)
description: Définit la couleur de la barre de l’indicateur de progression dans le contrôle de barre de progression.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508914"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="354b8-104">\_Message PBM SETBARCOLOR</span><span class="sxs-lookup"><span data-stu-id="354b8-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="354b8-105">Définit la couleur de la barre de l’indicateur de progression dans le contrôle de barre de progression.</span><span class="sxs-lookup"><span data-stu-id="354b8-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="354b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="354b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="354b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="354b8-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="354b8-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="354b8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="354b8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="354b8-110">Valeur **COLORREF** qui spécifie la nouvelle couleur de barre de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="354b8-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="354b8-111">Si vous spécifiez la \_ valeur CLR par défaut, la barre de progression utilise sa couleur de barre d’indicateur de progression par défaut.</span><span class="sxs-lookup"><span data-stu-id="354b8-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354b8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="354b8-112">Return value</span></span>

<span data-ttu-id="354b8-113">Retourne la couleur de la barre de l’indicateur de progression précédente, ou CLR \_ par défaut si la couleur de la barre de l’indicateur de progression est la couleur par défaut.</span><span class="sxs-lookup"><span data-stu-id="354b8-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="354b8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="354b8-114">Remarks</span></span>

<span data-ttu-id="354b8-115">Lorsque les styles visuels sont activés, ce message n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="354b8-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="354b8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="354b8-116">Requirements</span></span>



| <span data-ttu-id="354b8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="354b8-117">Requirement</span></span> | <span data-ttu-id="354b8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="354b8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="354b8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="354b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="354b8-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="354b8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="354b8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="354b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="354b8-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="354b8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="354b8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="354b8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="354b8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="354b8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





