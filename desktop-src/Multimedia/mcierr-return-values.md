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
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364008"
---
# <a name="mcierr-return-values"></a>MCIERR les valeurs de retour

Les fonctions [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) et [**mciSendString**](/previous-versions//dd757161(v=vs.85)) retournent zéro si elles réussissent ; Sinon, elles retournent une valeur **DWORD** qui contient l’une des valeurs d’erreur suivantes dans le mot de poids faible.

-   [Erreurs MCI générales](general-mci-errors.md)
-   [Erreurs mciSendString](mcisendstring-errors.md)
-   [Erreurs de vidéo numérique](digital-video-errors.md)
-   [Erreurs de Sequencer](sequencer-errors.md)
-   [Erreurs Waveform-Audio](waveform-audio-errors.md)

Vous pouvez obtenir une description des valeurs de retour individuelles en passant les valeurs de retour à la fonction [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .

 

 