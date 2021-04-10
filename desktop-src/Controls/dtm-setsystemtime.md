---
title: Message DTM_SETSYSTEMTIME (commctrl. h)
description: Définit l’heure dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetSystemtime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME les contrôles de message Windows
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942600"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="b71ec-105">\_Message DTM SETSYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="b71ec-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="b71ec-106">Définit l’heure dans un contrôle de sélecteur de dates et d’heures (PAO).</span><span class="sxs-lookup"><span data-stu-id="b71ec-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="b71ec-107">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="b71ec-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b71ec-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b71ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b71ec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b71ec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b71ec-110">Valeur qui spécifie l’action qui doit être effectuée.</span><span class="sxs-lookup"><span data-stu-id="b71ec-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="b71ec-111">Cette valeur doit être définie sur l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b71ec-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="b71ec-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71ec-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="b71ec-113">Signification</span><span class="sxs-lookup"><span data-stu-id="b71ec-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="b71ec-114"><dt>**GDT \_ valide**</dt></span><span class="sxs-lookup"><span data-stu-id="b71ec-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="b71ec-115">Définissez le contrôle PAO en fonction des données de la structure vers laquelle *lParam* pointe.</span><span class="sxs-lookup"><span data-stu-id="b71ec-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="b71ec-116"><dt>**GDT \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="b71ec-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="b71ec-117">Définissez le contrôle PAO sur « aucune date » et désactivez sa case à cocher.</span><span class="sxs-lookup"><span data-stu-id="b71ec-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="b71ec-118">Lorsque cet indicateur est spécifié, *lParam* est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b71ec-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="b71ec-119">Cet indicateur s’applique uniquement aux contrôles de PAO définis sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b71ec-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="b71ec-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b71ec-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b71ec-121">Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contenant l’heure système utilisée pour définir le contrôle de PAO.</span><span class="sxs-lookup"><span data-stu-id="b71ec-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b71ec-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b71ec-122">Return value</span></span>

<span data-ttu-id="b71ec-123">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b71ec-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b71ec-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b71ec-124">Requirements</span></span>



| <span data-ttu-id="b71ec-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b71ec-125">Requirement</span></span> | <span data-ttu-id="b71ec-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b71ec-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b71ec-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b71ec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b71ec-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b71ec-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b71ec-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b71ec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b71ec-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b71ec-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b71ec-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b71ec-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b71ec-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b71ec-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

