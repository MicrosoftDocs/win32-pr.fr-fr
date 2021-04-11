---
title: Message MCM_GETCOLOR (commctrl. h)
description: Récupère la couleur d’une partie donnée d’un contrôle calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetColor.
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105457"
---
# <a name="mcm_getcolor-message"></a><span data-ttu-id="2f025-105">Message de la \_ GETCOLOR MCM</span><span class="sxs-lookup"><span data-stu-id="2f025-105">MCM\_GETCOLOR message</span></span>

<span data-ttu-id="2f025-106">Récupère la couleur d’une partie donnée d’un contrôle calendrier mensuel.</span><span class="sxs-lookup"><span data-stu-id="2f025-106">Retrieves the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="2f025-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) .</span><span class="sxs-lookup"><span data-stu-id="2f025-107">You can send this message explicitly or by using the [**MonthCal\_GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f025-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f025-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f025-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f025-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f025-110">Valeur de type **int** spécifiant la couleur du calendrier mensuel à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2f025-110">Value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="2f025-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="2f025-111">This value can be one of the following:</span></span>



| <span data-ttu-id="2f025-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f025-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="2f025-113">Signification</span><span class="sxs-lookup"><span data-stu-id="2f025-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="2f025-114"><dt>**\_arrière-plan MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="2f025-115">Récupérez la couleur d’arrière-plan affichée entre les mois.</span><span class="sxs-lookup"><span data-stu-id="2f025-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="2f025-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="2f025-117">Récupérez la couleur d’arrière-plan affichée dans le mois.</span><span class="sxs-lookup"><span data-stu-id="2f025-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="2f025-118"><dt>**\_texte MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="2f025-119">Récupérez la couleur utilisée pour afficher le texte dans un mois.</span><span class="sxs-lookup"><span data-stu-id="2f025-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="2f025-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="2f025-121">Récupérez la couleur d’arrière-plan affichée dans le titre du calendrier.</span><span class="sxs-lookup"><span data-stu-id="2f025-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="2f025-122"><dt>**MCSC, \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="2f025-123">Récupérez la couleur utilisée pour afficher le texte dans le titre du calendrier.</span><span class="sxs-lookup"><span data-stu-id="2f025-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="2f025-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="2f025-125">Récupère la couleur utilisée pour afficher le texte du jour de l’en-tête et du jour de fin.</span><span class="sxs-lookup"><span data-stu-id="2f025-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="2f025-126">Les jours d’en-tête et de fin sont les jours des mois précédents et suivants qui apparaissent dans le calendrier du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="2f025-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f025-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f025-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f025-128">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="2f025-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f025-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f025-129">Return value</span></span>

<span data-ttu-id="2f025-130">Retourne une valeur **COLORREF** qui représente le paramètre de couleur pour la partie spécifiée du contrôle Month Calendar en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="2f025-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="2f025-131">Dans le cas contraire, ce message retourne-1.</span><span class="sxs-lookup"><span data-stu-id="2f025-131">Otherwise, this message returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f025-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f025-132">Requirements</span></span>



| <span data-ttu-id="2f025-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f025-133">Requirement</span></span> | <span data-ttu-id="2f025-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f025-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f025-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f025-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2f025-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f025-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f025-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f025-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2f025-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f025-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f025-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f025-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f025-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f025-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





