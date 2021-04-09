---
title: Message MCM_GETMAXTODAYWIDTH (commctrl. h)
description: Récupère la largeur maximale de \ 0034 ; Today \ 0034 ; chaîne dans un contrôle Month Calendar. Cela comprend le texte de l’étiquette et le texte de la date. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- MCM_GETMAXTODAYWIDTH les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741820"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="9e7ea-106">\_Message GETMAXTODAYWIDTH MCM</span><span class="sxs-lookup"><span data-stu-id="9e7ea-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="9e7ea-107">Récupère la largeur maximale de la chaîne « Today » dans un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="9e7ea-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="9e7ea-108">Cela comprend le texte de l’étiquette et le texte de la date.</span><span class="sxs-lookup"><span data-stu-id="9e7ea-108">This includes the label text and the date text.</span></span> <span data-ttu-id="9e7ea-109">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .</span><span class="sxs-lookup"><span data-stu-id="9e7ea-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e7ea-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e7ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7ea-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e7ea-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9e7ea-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9e7ea-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9e7ea-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e7ea-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9e7ea-114">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9e7ea-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7ea-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e7ea-115">Return value</span></span>

<span data-ttu-id="9e7ea-116">Retourne la largeur de la chaîne « Today », en pixels.</span><span class="sxs-lookup"><span data-stu-id="9e7ea-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7ea-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e7ea-117">Requirements</span></span>



| <span data-ttu-id="9e7ea-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e7ea-118">Requirement</span></span> | <span data-ttu-id="9e7ea-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e7ea-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7ea-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e7ea-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e7ea-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e7ea-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e7ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e7ea-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9e7ea-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e7ea-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9e7ea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e7ea-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7ea-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





