---
title: Message PBM_SETRANGE32 (commctrl. h)
description: Définit les valeurs minimale et maximale d’une barre de progression sur les valeurs 32 bits et redessine la barre pour refléter la nouvelle plage.
ms.assetid: 7958ea14-17b4-4c0e-97ec-b09fa0d36e8b
keywords:
- PBM_SETRANGE32 les contrôles de message Windows
topic_type:
- apiref
api_name:
- PBM_SETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55fcf91c794ec9ae3880d67f8df947f87fec413d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742532"
---
# <a name="pbm_setrange32-message"></a><span data-ttu-id="9fd3e-104">\_Message PBM SETRANGE32</span><span class="sxs-lookup"><span data-stu-id="9fd3e-104">PBM\_SETRANGE32 message</span></span>

<span data-ttu-id="9fd3e-105">Définit les valeurs minimale et maximale d’une barre de progression sur les valeurs 32 bits et redessine la barre pour refléter la nouvelle plage.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-105">Sets the minimum and maximum values for a progress bar to 32-bit values, and redraws the bar to reflect the new range.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fd3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fd3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd3e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd3e-108">Valeur de plage minimale.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-108">Minimum range value.</span></span> <span data-ttu-id="9fd3e-109">Par défaut, la valeur minimale est zéro.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-109">By default, the minimum value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="9fd3e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fd3e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd3e-111">Valeur de plage maximale.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-111">Maximum range value.</span></span> <span data-ttu-id="9fd3e-112">Cette valeur doit être supérieure à *wParam*.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-112">This value must be greater than *wParam*.</span></span> <span data-ttu-id="9fd3e-113">Par défaut, la valeur maximale est 100.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd3e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9fd3e-114">Return value</span></span>

<span data-ttu-id="9fd3e-115">Retourne une valeur **DWORD** qui contient la limite inférieure 16 bits précédente dans son [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et la limite supérieure 16 bits précédente dans son [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9fd3e-115">Returns a **DWORD** value that holds the previous 16-bit low limit in its [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the previous 16-bit high limit in its [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="9fd3e-116">Si les plages précédentes étaient des valeurs 32 bits, la valeur de retour est composée des **LOWORD** s des deux limites de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9fd3e-116">If the previous ranges were 32-bit values, the return value consists of the **LOWORD** s of both 32-bit limits.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fd3e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9fd3e-117">Remarks</span></span>

<span data-ttu-id="9fd3e-118">Pour récupérer les valeurs de 32 bits les plus élevées et les plus basses, utilisez le message [**PBM \_ GETRANGE**](pbm-getrange.md) .</span><span class="sxs-lookup"><span data-stu-id="9fd3e-118">To retrieve the entire high and low 32-bit values, use the [**PBM\_GETRANGE**](pbm-getrange.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd3e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fd3e-119">Requirements</span></span>



| <span data-ttu-id="9fd3e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fd3e-120">Requirement</span></span> | <span data-ttu-id="9fd3e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fd3e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd3e-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd3e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd3e-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fd3e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fd3e-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9fd3e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd3e-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9fd3e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fd3e-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fd3e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd3e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd3e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

