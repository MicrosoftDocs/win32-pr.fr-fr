---
title: MCIERR les valeurs de retour
description: MCIERR les valeurs de retour
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimédia, valeurs de retour MCIERR
- multimédias, valeurs de retour MCIERR
- Référence multimédia, valeurs de retour MCIERR
- référence pour les valeurs de retour multimédias, MCIERR
- MCIERR les valeurs de retour, à propos de
- mciSendCommand fonction)
- mciSendString fonction)
- Windows multimédia, erreurs
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
ms.openlocfilehash: 57fc8426b264f68d7a6ab793e365d529774c931e72d89536b40b22592728a2ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783409"
---
# <a name="mcierr-return-values"></a>MCIERR les valeurs de retour

Les fonctions [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) et [**mciSendString**](/previous-versions//dd757161(v=vs.85)) retournent zéro si elles réussissent ; Sinon, elles retournent une valeur **DWORD** qui contient l’une des valeurs d’erreur suivantes dans le mot de poids faible.

-   [Erreurs MCI générales](general-mci-errors.md)
-   [Erreurs mciSendString](mcisendstring-errors.md)
-   [Erreurs de vidéo numérique](digital-video-errors.md)
-   [Erreurs de Sequencer](sequencer-errors.md)
-   [Erreurs Waveform-Audio](waveform-audio-errors.md)

Vous pouvez obtenir une description des valeurs de retour individuelles en passant les valeurs de retour à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .

 

 