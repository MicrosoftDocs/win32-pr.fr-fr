---
title: MCIERR les valeurs de retour
description: MCIERR les valeurs de retour
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows Multimedia, MCIERR, valeurs de retour
- multimédias, valeurs de retour MCIERR
- Référence multimédia, valeurs de retour MCIERR
- référence pour les valeurs de retour multimédias, MCIERR
- MCIERR les valeurs de retour, à propos de
- mciSendCommand fonction)
- mciSendString fonction)
- Multimédia Windows, Erreurs
- multimédia, Erreurs
- Référence multimédia, Erreurs
- référence pour les éléments multimédias, Erreurs
- MCI (Media Control Interface), valeurs de retour MCIERR
- MCI (interface de contrôle multimédia), valeurs de retour MCIERR
- référence pour MCI, MCIERR les valeurs de retour
- Informations de référence sur MCI, valeurs de retour MCIERR
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106527147"
---
# <a name="mcierr-return-values"></a><span data-ttu-id="4b63e-122">MCIERR les valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4b63e-122">MCIERR Return Values</span></span>

<span data-ttu-id="4b63e-123">Les fonctions [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) et [**mciSendString**](/previous-versions//dd757161(v=vs.85)) retournent zéro si elles réussissent ; Sinon, elles retournent une valeur **DWORD** qui contient l’une des valeurs d’erreur suivantes dans le mot de poids faible.</span><span class="sxs-lookup"><span data-stu-id="4b63e-123">The [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) and [**mciSendString**](/previous-versions//dd757161(v=vs.85)) functions return zero if they are successful; otherwise, they return a **DWORD** value that contains one of the following error values in the low word.</span></span>

-   [<span data-ttu-id="4b63e-124">Erreurs MCI générales</span><span class="sxs-lookup"><span data-stu-id="4b63e-124">General MCI Errors</span></span>](general-mci-errors.md)
-   [<span data-ttu-id="4b63e-125">Erreurs mciSendString</span><span class="sxs-lookup"><span data-stu-id="4b63e-125">mciSendString Errors</span></span>](mcisendstring-errors.md)
-   [<span data-ttu-id="4b63e-126">Erreurs de vidéo numérique</span><span class="sxs-lookup"><span data-stu-id="4b63e-126">Digital-Video Errors</span></span>](digital-video-errors.md)
-   [<span data-ttu-id="4b63e-127">Erreurs de Sequencer</span><span class="sxs-lookup"><span data-stu-id="4b63e-127">Sequencer Errors</span></span>](sequencer-errors.md)
-   [<span data-ttu-id="4b63e-128">Erreurs Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="4b63e-128">Waveform-Audio Errors</span></span>](waveform-audio-errors.md)

<span data-ttu-id="4b63e-129">Vous pouvez obtenir une description des valeurs de retour individuelles en passant les valeurs de retour à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4b63e-129">You can obtain a description of individual return values by passing the return values to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function.</span></span>

 

 