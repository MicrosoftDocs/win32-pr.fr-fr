---
title: Message TDM_SET_PROGRESS_BAR_RANGE (commctrl. h)
description: Définit les valeurs minimale et maximale de la barre de progression dans une boîte de dialogue de tâche.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844365"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="8e731-104">Message de plage de la barre de progression de l' \_ ensemble TDM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8e731-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="8e731-105">Définit les valeurs minimale et maximale de la barre de progression dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="8e731-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e731-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e731-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e731-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e731-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e731-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8e731-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e731-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e731-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e731-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="8e731-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="8e731-111">Par défaut, la valeur minimale est zéro.</span><span class="sxs-lookup"><span data-stu-id="8e731-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="8e731-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="8e731-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="8e731-113">Par défaut, la valeur maximale est 100.</span><span class="sxs-lookup"><span data-stu-id="8e731-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e731-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e731-114">Return value</span></span>

<span data-ttu-id="8e731-115">Retourne les valeurs minimale et maximale précédentes, en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8e731-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="8e731-116">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient la valeur minimale et [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contient la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="8e731-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e731-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e731-117">Requirements</span></span>



| <span data-ttu-id="8e731-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e731-118">Requirement</span></span> | <span data-ttu-id="8e731-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e731-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e731-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e731-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e731-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e731-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e731-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e731-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e731-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8e731-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e731-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e731-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e731-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e731-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

