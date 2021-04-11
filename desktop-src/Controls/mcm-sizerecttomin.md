---
title: Message MCM_SIZERECTTOMIN (commctrl. h)
description: Calcule le nombre de calendriers qui tiennent dans le rectangle donné, puis retourne la taille minimale nécessaire pour qu’un rectangle tienne dans ce nombre de calendriers. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SizeRectToMin.
ms.assetid: d52a7f68-e0c9-4646-a4aa-97129dffeb5d
keywords:
- MCM_SIZERECTTOMIN les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SIZERECTTOMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f525f4cca9280b92fab0b9b86aa1d950ed990ef4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105982"
---
# <a name="mcm_sizerecttomin-message"></a><span data-ttu-id="09ba0-105">\_Message SIZERECTTOMIN MCM</span><span class="sxs-lookup"><span data-stu-id="09ba0-105">MCM\_SIZERECTTOMIN message</span></span>

<span data-ttu-id="09ba0-106">Calcule le nombre de calendriers qui tiennent dans le rectangle donné, puis retourne la taille minimale nécessaire pour qu’un rectangle tienne dans ce nombre de calendriers.</span><span class="sxs-lookup"><span data-stu-id="09ba0-106">Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars.</span></span> <span data-ttu-id="09ba0-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) .</span><span class="sxs-lookup"><span data-stu-id="09ba0-107">You can send this message explicitly or by using the [**MonthCal\_SizeRectToMin**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_sizerecttomin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="09ba0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09ba0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ba0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09ba0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09ba0-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="09ba0-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="09ba0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09ba0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="09ba0-112">Sur entrée, contient un pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui décrit une région qui est supérieure ou égale à la taille nécessaire pour s’adapter au nombre souhaité de calendriers.</span><span class="sxs-lookup"><span data-stu-id="09ba0-112">On entry, contains a pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars.</span></span> <span data-ttu-id="09ba0-113">Lorsque cette fonction est retournée, contient la structure **Rect** minimale qui correspond à ce nombre de calendriers.</span><span class="sxs-lookup"><span data-stu-id="09ba0-113">When this function returns, contains the minimum **RECT** structure that fits this number of calendars.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09ba0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09ba0-114">Return value</span></span>

<span data-ttu-id="09ba0-115">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="09ba0-115">Unused.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ba0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09ba0-116">Requirements</span></span>



| <span data-ttu-id="09ba0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09ba0-117">Requirement</span></span> | <span data-ttu-id="09ba0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="09ba0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09ba0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ba0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="09ba0-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09ba0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09ba0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ba0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="09ba0-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09ba0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09ba0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="09ba0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ba0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ba0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

