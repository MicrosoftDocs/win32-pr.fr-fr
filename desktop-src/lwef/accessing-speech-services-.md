---
title: Accès aux services vocaux (contrôle Microsoft Agent)
description: En savoir plus sur l’accès aux services vocaux avec le contrôle Microsoft Agent. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617da522912e2fbae361fb3addf569d5164894fc2b98a901686b2458d4d0a8e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114939"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Accès aux services vocaux (contrôle Microsoft Agent)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Bien que les services de Microsoft Agent incluent la prise en charge de l’entrée vocale, un moteur de reconnaissance vocale de commande et de contrôle compatible doit être installé pour accéder aux services d’entrée vocale de l’agent. De même, si vous souhaitez utiliser les services de reconnaissance vocale de Microsoft Agent pour prendre en charge la synthèse vocale d’un caractère, vous devez installer un moteur de reconnaissance vocale de conversion de texte en parole (TTS) compatible pour votre caractère.

Pour activer la prise en charge de l’entrée vocale dans votre application, définissez un objet de [**commande**](https://www.bing.com/search?q=**Command**) et définissez sa propriété [**Voice**](https://www.bing.com/search?q=**Voice**) . Agent chargera automatiquement les services vocaux, de sorte que lorsque l’utilisateur appuie sur la touche d’écoute ou que vous appelez [**Listen**](https://www.bing.com/search?q=**Listen**), le moteur de reconnaissance vocale est chargé. Par défaut, l' [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) du caractère détermine quel moteur est chargé. L’agent tente de charger le premier moteur que l’API Microsoft Speech (SAPI) retourne comme correspondant à cette langue. Utilisez [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) si vous souhaitez charger un moteur spécifique.

Pour activer la sortie de conversion de texte par synthèse vocale, utilisez la méthode [**Speak**](https://www.bing.com/search?q=**Speak**) . L’agent tente automatiquement de charger un moteur qui correspond à l' [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)du caractère. Si la définition du caractère comprend un ID de mode de moteur TTS spécifique et que le moteur est disponible et correspond au **LanguageID** du caractère, l’agent charge ce moteur pour le caractère. Si ce n’est pas le cas, il charge le premier moteur TTS que SAPI retourne comme correspondant au paramètre de langue du caractère. Vous pouvez également utiliser [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) pour charger un moteur spécifique.

En règle générale, l’agent charge la reconnaissance vocale lorsque le mode d’écoute est lancé et un moteur de conversion de texte par synthèse vocale lorsque la fonction [**Speak**](https://www.bing.com/search?q=**Speak**) est appelée pour la première fois. Toutefois, si vous souhaitez précharger le moteur de reconnaissance vocale, vous interrogez les propriétés relatives aux interfaces vocales. Par exemple, l’interrogation de [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) ou [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) va tenter de charger ce type de moteur.

Étant donné que les services vocaux de Microsoft Agent sont basés sur l’API Microsoft Speech, vous pouvez utiliser n’importe quel moteur prenant en charge les interfaces vocales requises.

 

 




