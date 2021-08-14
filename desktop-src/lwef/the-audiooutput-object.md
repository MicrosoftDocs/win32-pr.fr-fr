---
title: Objet AudioOutput
description: Objet AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bfef883e5cb40d0a72ec4d848ad0d77f63f58aaeefd907f632e16798be4397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474949"
---
# <a name="the-audiooutput-object"></a>Objet AudioOutput

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Cet objet permet d’accéder aux propriétés de sortie audio gérées par le serveur. Les propriétés sont en lecture seule, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft.

Si vous déclarez une variable objet de type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), vous ne pourrez pas accéder à toutes les propriétés de l’objet [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) . Tandis que agent prend également en charge [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), cette dernière interface est fournie uniquement à des fins de compatibilité descendante et prend en charge uniquement les propriétés des versions précédentes.

-   [**Activé**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Statut**](status-property.md)

 

 