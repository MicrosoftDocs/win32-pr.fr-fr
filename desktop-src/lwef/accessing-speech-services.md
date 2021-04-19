---
title: Accès aux services vocaux (interface du serveur Microsoft Agent)
description: Accès aux services vocaux
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb4afb2b05ca13c52d49508c3c25b7e02da676
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380803"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Accès aux services vocaux (interface du serveur Microsoft Agent)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Bien que les services de Microsoft Agent incluent la prise en charge de l’entrée vocale, un moteur de reconnaissance vocale de commande et de contrôle compatible doit être installé pour accéder aux services d’entrée vocale de l’agent. De même, si vous souhaitez utiliser les services de reconnaissance vocale de Microsoft Agent pour prendre en charge la synthèse vocale d’un caractère, vous devez installer un moteur de reconnaissance vocale de conversion de texte en parole (TTS) compatible pour votre caractère. Étant donné que les services de reconnaissance vocale de Microsoft Agent sont basés sur l’API Microsoft Speech (SAPI), vous pouvez utiliser tous les moteurs compatibles avec les interfaces vocales requises.

Pour activer la prise en charge de l’entrée vocale dans votre application, définissez un objet de [**commande**](https://www.bing.com/search?q=**Command**) et définissez sa propriété [**Voice**](https://www.bing.com/search?q=**Voice**) . Microsoft Agent chargera automatiquement les services vocaux, de sorte que lorsque l’utilisateur appuie sur la touche d’écoute ou que vous appelez [**Listen**](https://www.bing.com/search?q=**Listen**), le moteur de reconnaissance vocale est chargé. Par défaut, l’ID de langue du caractère détermine quel moteur est chargé. L’agent tente de charger le premier moteur que SAPI retourne comme correspondant à cette langue. Utilisez **IAgentCharacterEx :: SetSRModeID** si vous souhaitez charger un moteur spécifique.

Pour activer la sortie de conversion de texte par synthèse vocale, utilisez la méthode [**Speak**](https://www.bing.com/search?q=**Speak**) . Microsoft Agent tente automatiquement de charger un moteur qui correspond à l’ID de langue du caractère. Si la définition du caractère comprend un ID de mode de moteur TTS spécifique et que le moteur est disponible et correspond à l’ID de langue du caractère, l’agent charge ce moteur pour le caractère. Si ce n’est pas le cas, l’agent charge le premier moteur TTS retourné par SAPI comme correspondant au paramètre de langue du caractère. Vous pouvez également utiliser **IAgentCharacterEx :: SetTTSModeID** pour charger un moteur spécifique.

En règle générale, Microsoft agent charge un moteur de reconnaissance vocale lorsque le mode d’écoute est initié et charge un moteur de synthèse vocale lorsque la fonction [**Speak**](https://www.bing.com/search?q=**Speak**) est appelée pour la première fois. Toutefois, si vous souhaitez précharger le moteur de reconnaissance vocale, vous pouvez effectuer cette opération en interrogeant les propriétés relatives aux interfaces vocales. Par exemple, si vous appelez **IAgentCharacterEx :: GetSRModeID** ou **IAgentCharacterEx :: GetTTSModeID** , vous tenterez de charger ce type de moteur.

 

 




