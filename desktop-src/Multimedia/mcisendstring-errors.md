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
ms.openlocfilehash: 27d7603821a20dd154548cdf3cc69b84d54df1d549e9f3c87362e10a03e8e9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783439"
---
# <a name="mcisendstring-errors"></a>Erreurs mciSendString

Les erreurs suivantes sont retournées par la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , mais pas par [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):



| Valeur                             | Signification                                           |
|-----------------------------------|---------------------------------------------------|
| MCIERR \_ constante incorrecte \_             | La valeur spécifiée pour un paramètre est inconnue.   |
| MCIERR \_ entier incorrect \_              | Un entier dans la commande n’est pas valide ou est manquant. |
| MCIERR \_ les \_ indicateurs en double          | Un indicateur ou une valeur a été spécifié deux fois.              |
| MCIERR \_ \_ chaîne de commande manquante \_  | Aucune commande n’a été spécifiée.                         |
| MCIERR \_ \_ nom de périphérique manquant \_     | Aucun nom de périphérique n’a été spécifié.                     |
| MCIERR \_ \_ argument de chaîne manquant \_ | Il manque une valeur de chaîne dans la commande.      |
| MCIERR \_ New \_ requiert un \_ alias      | Un alias doit être utilisé avec le nom du nouveau périphérique. |
| MCIERR \_ pas \_ de \_ guillemet fermant        | Un guillemet fermant est manquant.              |
| MCIERR \_ notifier \_ lors de l' \_ \_ ouverture automatique    | L’indicateur « Notify » est non conforme avec l’ouverture automatique.      |
| \_dépassement du paramètre MCIERR \_           | La chaîne de sortie n’était pas suffisamment longue.            |
| \_analyseur MCIERR \_ interne          | Une erreur d’analyseur interne s’est produite.                |
| MCIERR \_ \_ mot clé non reconnu     | Un paramètre de commande inconnu a été spécifié.       |



 

 

 