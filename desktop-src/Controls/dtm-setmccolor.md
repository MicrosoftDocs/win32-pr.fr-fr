---
title: Message DTM_SETMCCOLOR (commctrl. h)
description: Définit la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetMonthCalColor.
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742564"
---
# <a name="dtm_setmccolor-message"></a><span data-ttu-id="4ab71-105">\_Message DTM SETMCCOLOR</span><span class="sxs-lookup"><span data-stu-id="4ab71-105">DTM\_SETMCCOLOR message</span></span>

<span data-ttu-id="4ab71-106">Définit la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="4ab71-106">Sets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="4ab71-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="4ab71-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ab71-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ab71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab71-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ab71-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ab71-110">Valeur de type **int** spécifiant la couleur du calendrier mensuel à définir.</span><span class="sxs-lookup"><span data-stu-id="4ab71-110">A value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="4ab71-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ab71-111">This value can be one of the following:</span></span>



| <span data-ttu-id="4ab71-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ab71-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="4ab71-113">Signification</span><span class="sxs-lookup"><span data-stu-id="4ab71-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="4ab71-114"><dt>**\_arrière-plan MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="4ab71-115">Définissez la couleur d’arrière-plan affichée entre les mois.</span><span class="sxs-lookup"><span data-stu-id="4ab71-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="4ab71-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="4ab71-117">Définissez la couleur d’arrière-plan affichée dans le mois.</span><span class="sxs-lookup"><span data-stu-id="4ab71-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="4ab71-118"><dt>**\_texte MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="4ab71-119">Définissez la couleur utilisée pour afficher le texte dans un mois.</span><span class="sxs-lookup"><span data-stu-id="4ab71-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="4ab71-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="4ab71-121">Définissez la couleur d’arrière-plan affichée dans le titre du calendrier.</span><span class="sxs-lookup"><span data-stu-id="4ab71-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="4ab71-122"><dt>**MCSC, \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="4ab71-123">Définissez la couleur utilisée pour afficher le texte dans le titre du calendrier.</span><span class="sxs-lookup"><span data-stu-id="4ab71-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="4ab71-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="4ab71-125">Définissez la couleur utilisée pour afficher le texte du jour de l’en-tête et du jour de fin.</span><span class="sxs-lookup"><span data-stu-id="4ab71-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="4ab71-126">Les jours d’en-tête et de fin sont les jours des mois précédents et suivants qui apparaissent dans le calendrier du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="4ab71-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ab71-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ab71-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ab71-128">Valeur **COLORREF** représentant la couleur qui sera définie pour la zone spécifiée du calendrier du mois.</span><span class="sxs-lookup"><span data-stu-id="4ab71-128">A **COLORREF** value representing the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ab71-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ab71-129">Return value</span></span>

<span data-ttu-id="4ab71-130">Retourne une valeur **COLORREF** qui représente le paramètre de couleur précédent pour la partie spécifiée du contrôle Month Calendar en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="4ab71-130">Returns a **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="4ab71-131">Dans le cas contraire, le message retourne-1.</span><span class="sxs-lookup"><span data-stu-id="4ab71-131">Otherwise, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ab71-132">Notes</span><span class="sxs-lookup"><span data-stu-id="4ab71-132">Remarks</span></span>

<span data-ttu-id="4ab71-133">Lorsque les styles visuels sont activés, ce message n’a aucun effet, sauf lorsque *wParam* est l' \_ arrière-plan MCSC.</span><span class="sxs-lookup"><span data-stu-id="4ab71-133">When visual styles are enabled, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab71-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ab71-134">Requirements</span></span>



| <span data-ttu-id="4ab71-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ab71-135">Requirement</span></span> | <span data-ttu-id="4ab71-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ab71-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab71-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ab71-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab71-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ab71-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ab71-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ab71-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab71-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4ab71-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ab71-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="4ab71-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ab71-142"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ab71-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





