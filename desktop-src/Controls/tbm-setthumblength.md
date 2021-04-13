---
title: Message TBM_SETTHUMBLENGTH (commctrl. h)
description: Définit la longueur du curseur dans un TrackBar. Ce message est ignoré si le TrackBar n’a pas le \_ style tbs multiple.
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509217"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="377eb-105">\_Message TBM SETTHUMBLENGTH</span><span class="sxs-lookup"><span data-stu-id="377eb-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="377eb-106">Définit la longueur du curseur dans un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="377eb-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="377eb-107">Ce message est ignoré si le TrackBar n’a pas le style [**tbs \_ multiple**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="377eb-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="377eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="377eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="377eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="377eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="377eb-110">Longueur, en pixels, du curseur.</span><span class="sxs-lookup"><span data-stu-id="377eb-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="377eb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="377eb-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="377eb-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="377eb-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="377eb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="377eb-113">Return value</span></span>

<span data-ttu-id="377eb-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="377eb-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="377eb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="377eb-115">Requirements</span></span>



| <span data-ttu-id="377eb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="377eb-116">Requirement</span></span> | <span data-ttu-id="377eb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="377eb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="377eb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="377eb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="377eb-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="377eb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="377eb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="377eb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="377eb-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="377eb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="377eb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="377eb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="377eb-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="377eb-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="377eb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="377eb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="377eb-125">**TBM \_ GETTHUMBLENGTH**</span><span class="sxs-lookup"><span data-stu-id="377eb-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





