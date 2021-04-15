---
title: Message DTM_GETMCCOLOR (commctrl. h)
description: Obtient la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCalColor.
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- DTM_GETMCCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479461"
---
# <a name="dtm_getmccolor-message"></a><span data-ttu-id="9b30b-105">\_Message DTM GETMCCOLOR</span><span class="sxs-lookup"><span data-stu-id="9b30b-105">DTM\_GETMCCOLOR message</span></span>

<span data-ttu-id="9b30b-106">Obtient la couleur d’une partie donnée du calendrier du mois dans un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="9b30b-106">Gets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="9b30b-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) .</span><span class="sxs-lookup"><span data-stu-id="9b30b-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b30b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b30b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b30b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b30b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b30b-110">Valeur de type **int** spécifiant la couleur du calendrier mensuel à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9b30b-110">A value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="9b30b-111">Cette valeur peut être l'une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="9b30b-111">This value can be one of the following:</span></span>



| <span data-ttu-id="9b30b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b30b-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="9b30b-113">Signification</span><span class="sxs-lookup"><span data-stu-id="9b30b-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="9b30b-114"><dt>**\_arrière-plan MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="9b30b-115">Récupérez la couleur d’arrière-plan affichée entre les mois.</span><span class="sxs-lookup"><span data-stu-id="9b30b-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="9b30b-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="9b30b-117">Récupérez la couleur d’arrière-plan affichée dans le mois.</span><span class="sxs-lookup"><span data-stu-id="9b30b-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="9b30b-118"><dt>**\_texte MCSC**</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="9b30b-119">Récupérez la couleur utilisée pour afficher le texte dans un mois.</span><span class="sxs-lookup"><span data-stu-id="9b30b-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="9b30b-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="9b30b-121">Récupérez la couleur d’arrière-plan affichée dans le titre du calendrier.</span><span class="sxs-lookup"><span data-stu-id="9b30b-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="9b30b-122"><dt>**MCSC, \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="9b30b-123">Récupérez la couleur utilisée pour afficher le texte dans le titre du calendrier.</span><span class="sxs-lookup"><span data-stu-id="9b30b-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="9b30b-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="9b30b-125">Récupère la couleur utilisée pour afficher le texte du jour de l’en-tête et du jour de fin.</span><span class="sxs-lookup"><span data-stu-id="9b30b-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="9b30b-126">Les jours d’en-tête et de fin sont les jours des mois précédents et suivants qui apparaissent dans le calendrier du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="9b30b-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9b30b-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b30b-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9b30b-128">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="9b30b-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b30b-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b30b-129">Return value</span></span>

<span data-ttu-id="9b30b-130">Retourne une valeur **COLORREF** qui représente le paramètre de couleur pour la partie spécifiée du contrôle Month Calendar en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="9b30b-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="9b30b-131">Le message retourne-1 en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="9b30b-131">The message returns -1 if unsuccessful.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b30b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b30b-132">Requirements</span></span>



| <span data-ttu-id="9b30b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b30b-133">Requirement</span></span> | <span data-ttu-id="9b30b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b30b-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b30b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b30b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9b30b-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b30b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b30b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b30b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9b30b-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9b30b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b30b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b30b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b30b-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b30b-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





