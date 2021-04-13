---
title: IAgentSpeechInputProperties
description: IAgentSpeechInputProperties
ms.assetid: 87bfc8c4-473b-4df9-becd-e90db12dae51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c6a83ed488d3ff95914c25fd518862740951ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379564"
---
# <a name="iagentspeechinputproperties"></a>IAgentSpeechInputProperties

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

IAgentSpeechInputProperties fournit l’accès aux propriétés d’entrée vocale gérées par le serveur. La plupart des propriétés sont en lecture seule pour les applications clientes, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft. Le serveur Microsoft Agent retourne des valeurs uniquement si un moteur de reconnaissance vocale compatible a été installé et est activé. L’interrogation de ces propriétés tente de démarrer le moteur de reconnaissance vocale.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentSpeechInputProperties                                     | Description                                               |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**GetEnabled**](iagentspeechinputproperties--getenabled.md)           | Retourne une valeur indiquant si le moteur de reconnaissance vocale est activé. |
| [**GetHotKey**](iagentspeechinputproperties--gethotkey.md)             | Retourne l’affectation de clé actuelle de la clé d’écoute.  |
| [**GetListeningTip**](iagentspeechinputproperties--getlisteningtip.md) | Retourne une valeur indiquant si l’info-bulle d’écoute est activée.             |



 

Les méthodes [**GetInstalled**](https://www.bing.com/search?q=**GetInstalled**), [**GetLCID**](https://www.bing.com/search?q=**GetLCID**), [**GetEngine**](https://www.bing.com/search?q=**GetEngine**)et [**SetEngine**](https://www.bing.com/search?q=**SetEngine**) (prises en charge dans les versions antérieures de Microsoft Agent) sont toujours prises en charge pour la compatibilité descendante. Toutefois, les méthodes ne sont pas extraites et ne retournent pas de valeurs utiles. Utilisez [**GetSRModeID**](https://www.bing.com/search?q=**GetSRModeID**) et [**SetSRModeID**](https://www.bing.com/search?q=**SetSRModeID**) pour interroger et définir le moteur de reconnaissance vocale à utiliser avec le caractère. Gardez à l’esprit que le moteur doit correspondre au paramètre de langue actuel du caractère.

 

 




