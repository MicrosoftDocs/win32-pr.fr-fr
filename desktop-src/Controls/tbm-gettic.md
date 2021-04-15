---
title: Message TBM_GETTIC (commctrl. h)
description: Récupère la position logique d’une graduation dans un TrackBar. La position logique peut être l’une des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position de curseur maximale.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d534d5100e20cc544c31fca2fc9e49cda3bd976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465362"
---
# <a name="tbm_gettic-message"></a><span data-ttu-id="1842f-105">\_Message TBM GETTIC</span><span class="sxs-lookup"><span data-stu-id="1842f-105">TBM\_GETTIC message</span></span>

<span data-ttu-id="1842f-106">Récupère la position logique d’une graduation dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="1842f-106">Retrieves the logical position of a tick mark in a trackbar.</span></span> <span data-ttu-id="1842f-107">La position logique peut être l’une des valeurs entières dans la plage de la plage de la barre de défilement minimale à la position de curseur maximale.</span><span class="sxs-lookup"><span data-stu-id="1842f-107">The logical position can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="1842f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1842f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1842f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1842f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1842f-110">Index de base zéro identifiant une graduation.</span><span class="sxs-lookup"><span data-stu-id="1842f-110">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="1842f-111">Les index valides se trouvent dans la plage comprise entre zéro et deux moins que le nombre de cycles renvoyé par le message [**TBM \_ GETNUMTICS**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="1842f-111">Valid indexes are in the range from zero to two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="1842f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1842f-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1842f-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="1842f-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1842f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1842f-114">Return value</span></span>

<span data-ttu-id="1842f-115">Retourne la position logique de la graduation spécifiée, ou-1 si *wParam* ne spécifie pas d’index valide.</span><span class="sxs-lookup"><span data-stu-id="1842f-115">Returns the logical position of the specified tick mark, or -1 if *wParam* does not specify a valid index.</span></span>

## <a name="requirements"></a><span data-ttu-id="1842f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1842f-116">Requirements</span></span>



| <span data-ttu-id="1842f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1842f-117">Requirement</span></span> | <span data-ttu-id="1842f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1842f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1842f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1842f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1842f-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1842f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1842f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1842f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1842f-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1842f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1842f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1842f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1842f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1842f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





