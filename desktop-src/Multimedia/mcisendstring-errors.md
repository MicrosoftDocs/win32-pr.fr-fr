---
title: Erreurs mciSendString
description: Erreurs mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR les valeurs de retour, erreurs mciSendString
- Référence multimédia, erreurs de mciSendString
- référence pour les erreurs multimédias, mciSendString
- MCI (Media Control Interface), erreurs mciSendString
- MCI (Media Control Interface), erreurs mciSendString
- informations de référence sur MCI, erreurs mciSendString
- Informations de référence sur MCI, erreurs mciSendString
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
- Erreurs mciSendString
- mciSendString fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842217"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="47953-116">Erreurs mciSendString</span><span class="sxs-lookup"><span data-stu-id="47953-116">mciSendString Errors</span></span>

<span data-ttu-id="47953-117">Les erreurs suivantes sont retournées par la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , mais pas par [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="47953-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="47953-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="47953-118">Value</span></span>                             | <span data-ttu-id="47953-119">Signification</span><span class="sxs-lookup"><span data-stu-id="47953-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="47953-120">MCIERR \_ constante incorrecte \_</span><span class="sxs-lookup"><span data-stu-id="47953-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="47953-121">La valeur spécifiée pour un paramètre est inconnue.</span><span class="sxs-lookup"><span data-stu-id="47953-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="47953-122">MCIERR \_ entier incorrect \_</span><span class="sxs-lookup"><span data-stu-id="47953-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="47953-123">Un entier dans la commande n’est pas valide ou est manquant.</span><span class="sxs-lookup"><span data-stu-id="47953-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="47953-124">MCIERR \_ les \_ indicateurs en double</span><span class="sxs-lookup"><span data-stu-id="47953-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="47953-125">Un indicateur ou une valeur a été spécifié deux fois.</span><span class="sxs-lookup"><span data-stu-id="47953-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="47953-126">MCIERR \_ \_ chaîne de commande manquante \_</span><span class="sxs-lookup"><span data-stu-id="47953-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="47953-127">Aucune commande n’a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="47953-127">No command was specified.</span></span>                         |
| <span data-ttu-id="47953-128">MCIERR \_ \_ nom de périphérique manquant \_</span><span class="sxs-lookup"><span data-stu-id="47953-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="47953-129">Aucun nom de périphérique n’a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="47953-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="47953-130">MCIERR \_ \_ argument de chaîne manquant \_</span><span class="sxs-lookup"><span data-stu-id="47953-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="47953-131">Il manque une valeur de chaîne dans la commande.</span><span class="sxs-lookup"><span data-stu-id="47953-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="47953-132">MCIERR \_ New \_ requiert un \_ alias</span><span class="sxs-lookup"><span data-stu-id="47953-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="47953-133">Un alias doit être utilisé avec le nom du nouveau périphérique.</span><span class="sxs-lookup"><span data-stu-id="47953-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="47953-134">MCIERR \_ pas \_ de \_ guillemet fermant</span><span class="sxs-lookup"><span data-stu-id="47953-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="47953-135">Un guillemet fermant est manquant.</span><span class="sxs-lookup"><span data-stu-id="47953-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="47953-136">MCIERR \_ notifier \_ lors de l' \_ \_ ouverture automatique</span><span class="sxs-lookup"><span data-stu-id="47953-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="47953-137">L’indicateur « Notify » est non conforme avec l’ouverture automatique.</span><span class="sxs-lookup"><span data-stu-id="47953-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="47953-138">\_dépassement du paramètre MCIERR \_</span><span class="sxs-lookup"><span data-stu-id="47953-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="47953-139">La chaîne de sortie n’était pas suffisamment longue.</span><span class="sxs-lookup"><span data-stu-id="47953-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="47953-140">\_analyseur MCIERR \_ interne</span><span class="sxs-lookup"><span data-stu-id="47953-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="47953-141">Une erreur d’analyseur interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="47953-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="47953-142">MCIERR \_ \_ mot clé non reconnu</span><span class="sxs-lookup"><span data-stu-id="47953-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="47953-143">Un paramètre de commande inconnu a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="47953-143">An unknown command parameter was specified.</span></span>       |



 

 

 