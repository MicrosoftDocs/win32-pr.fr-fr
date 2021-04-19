---
title: Message TCM_SETPADDING (commctrl. h)
description: Définit la quantité d’espace (remplissage) autour de l’icône et de l’étiquette de chaque onglet dans un contrôle onglet. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro TabCtrl SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106531609"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="05681-105">\_Message SETPADDING TCM</span><span class="sxs-lookup"><span data-stu-id="05681-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="05681-106">Définit la quantité d’espace (remplissage) autour de l’icône et de l’étiquette de chaque onglet dans un contrôle onglet.</span><span class="sxs-lookup"><span data-stu-id="05681-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="05681-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .</span><span class="sxs-lookup"><span data-stu-id="05681-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="05681-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05681-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05681-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05681-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05681-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est une valeur **int** qui spécifie la quantité de remplissage horizontal, en pixels.</span><span class="sxs-lookup"><span data-stu-id="05681-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="05681-111">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) est une valeur **int** qui spécifie la quantité de remplissage vertical, en pixels.</span><span class="sxs-lookup"><span data-stu-id="05681-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05681-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05681-112">Return value</span></span>

<span data-ttu-id="05681-113">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="05681-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="05681-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05681-114">Requirements</span></span>



| <span data-ttu-id="05681-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05681-115">Requirement</span></span> | <span data-ttu-id="05681-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="05681-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05681-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05681-117">Minimum supported client</span></span><br/> | <span data-ttu-id="05681-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05681-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05681-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05681-119">Minimum supported server</span></span><br/> | <span data-ttu-id="05681-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05681-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05681-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="05681-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="05681-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05681-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

