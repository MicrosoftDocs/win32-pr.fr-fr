---
title: Message TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indique si la barre de progression hébergée d’une boîte de dialogue de tâche doit être affichée en mode palissade.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105970"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="86cc8-104">\_Message de \_ barre de \_ progression du texte défilant de l’ensemble TDM \_</span><span class="sxs-lookup"><span data-stu-id="86cc8-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="86cc8-105">Indique si la barre de progression hébergée d’une boîte de dialogue de tâche doit être affichée en mode palissade.</span><span class="sxs-lookup"><span data-stu-id="86cc8-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="86cc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86cc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86cc8-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86cc8-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cc8-108">Valeur **booléenne** qui indique si la barre de progression doit être affichée en mode texte défilant.</span><span class="sxs-lookup"><span data-stu-id="86cc8-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="86cc8-109">La valeur **true** active le mode texte défilant, tandis que la valeur **false** désactive le mode texte défilant.</span><span class="sxs-lookup"><span data-stu-id="86cc8-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="86cc8-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="86cc8-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86cc8-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="86cc8-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86cc8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86cc8-112">Return value</span></span>

<span data-ttu-id="86cc8-113">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="86cc8-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="86cc8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="86cc8-114">Remarks</span></span>

<span data-ttu-id="86cc8-115">Pour plus d’informations sur le mode texte défilant, consultez [contrôle de barre de progression](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="86cc8-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86cc8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86cc8-116">Requirements</span></span>



| <span data-ttu-id="86cc8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86cc8-117">Requirement</span></span> | <span data-ttu-id="86cc8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="86cc8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86cc8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86cc8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86cc8-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86cc8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86cc8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86cc8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86cc8-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86cc8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86cc8-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="86cc8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="86cc8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86cc8-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





