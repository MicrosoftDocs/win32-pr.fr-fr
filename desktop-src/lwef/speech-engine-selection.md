---
title: Sélection du moteur de reconnaissance vocale
description: Sélection du moteur de reconnaissance vocale
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839862"
---
# <a name="speech-engine-selection"></a>Sélection du moteur de reconnaissance vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le paramètre ID de langue d’un caractère détermine son langage d’entrée vocale par défaut. Microsoft Agent demande SAPI pour un moteur installé qui correspond à cette langue. Si une application cliente ne spécifie pas de préférence de langue, Microsoft Agent tente de trouver un moteur de reconnaissance vocale qui correspond à l’ID de langue par défaut de l’utilisateur (à l’aide de l’ID de langue majeur, puis de l’ID de langue mineure). Si aucun moteur ne correspond à cette langue, la reconnaissance vocale est désactivée pour ce caractère.

Vous pouvez également demander un moteur de reconnaissance vocale spécifique en spécifiant son ID de mode (à l’aide de la propriété Character [**SRModeID**](srmodeid-property.md) ). Toutefois, si l’ID de langue de cet ID de mode ne correspond pas au paramètre de langue du client, l’appel échoue (génère une erreur dans le contrôle). Le moteur de reconnaissance vocale conserve alors le dernier moteur correctement défini par le client, ou s’il n’en a pas, le moteur qui correspond à l’ID de langue du système actuel. S’il n’y a toujours aucune correspondance, l’entrée vocale n’est pas disponible pour ce client.

Microsoft agent charge automatiquement un moteur de reconnaissance vocale lorsque l’entrée vocale est lancée par un utilisateur en appuyant sur la touche d’écoute ou lorsque le client d’entrée-actif appelle la méthode [**Listen**](listen-method.md) . Toutefois, un moteur peut également être chargé lors de la définition ou de l’interrogation de son ID de mode, lors de la définition ou de l’interrogation des propriétés de la fenêtre commandes vocales, lors de l’interrogation de [**SRStatus**](srstatus-property.md)ou lorsque la reconnaissance vocale est activée et que l’utilisateur affiche la page d’entrée vocale des options de caractères avancés. Toutefois, Microsoft Agent ne continue de charger que les moteurs de reconnaissance vocale que les clients utilisent.

 

 




