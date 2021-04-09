---
title: Message TBM_SETTICFREQ (commctrl. h)
description: Définit la fréquence d’intervalle des graduations d’un TrackBar.
ms.assetid: c391260c-d6c2-4b6a-84e8-7fe5d734035b
keywords:
- TBM_SETTICFREQ les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETTICFREQ
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a555a7803e663fa1708fc02214deecbb05aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032610"
---
# <a name="tbm_setticfreq-message"></a><span data-ttu-id="88db6-104">\_Message TBM SETTICFREQ</span><span class="sxs-lookup"><span data-stu-id="88db6-104">TBM\_SETTICFREQ message</span></span>

<span data-ttu-id="88db6-105">Définit la fréquence d’intervalle des graduations d’un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="88db6-105">Sets the interval frequency for tick marks in a trackbar.</span></span> <span data-ttu-id="88db6-106">Par exemple, si la fréquence est définie sur deux, une graduation est affichée pour chaque autre incrément dans la plage du TrackBar.</span><span class="sxs-lookup"><span data-stu-id="88db6-106">For example, if the frequency is set to two, a tick mark is displayed for every other increment in the trackbar's range.</span></span> <span data-ttu-id="88db6-107">Le paramètre par défaut de la fréquence est un ; autrement dit, chaque incrément de la plage est associé à une graduation.</span><span class="sxs-lookup"><span data-stu-id="88db6-107">The default setting for the frequency is one; that is, every increment in the range is associated with a tick mark.</span></span>

## <a name="parameters"></a><span data-ttu-id="88db6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88db6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88db6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88db6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88db6-110">Fréquence des graduations.</span><span class="sxs-lookup"><span data-stu-id="88db6-110">Frequency of the tick marks.</span></span>

</dd> <dt>

<span data-ttu-id="88db6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88db6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="88db6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="88db6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88db6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88db6-113">Return value</span></span>

<span data-ttu-id="88db6-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="88db6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88db6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="88db6-115">Remarks</span></span>

<span data-ttu-id="88db6-116">Le TrackBar doit avoir le style des [**\_ graduations tbs**](trackbar-control-styles.md) pour utiliser ce message.</span><span class="sxs-lookup"><span data-stu-id="88db6-116">The trackbar must have the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) style to use this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="88db6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88db6-117">Requirements</span></span>



| <span data-ttu-id="88db6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88db6-118">Requirement</span></span> | <span data-ttu-id="88db6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="88db6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88db6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88db6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="88db6-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88db6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="88db6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88db6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="88db6-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88db6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="88db6-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="88db6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="88db6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="88db6-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





