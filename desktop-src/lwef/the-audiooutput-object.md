---
title: Objet AudioOutput
description: Objet AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381952"
---
# <a name="the-audiooutput-object"></a>Objet AudioOutput

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Cet objet permet d’accéder aux propriétés de sortie audio gérées par le serveur. Les propriétés sont en lecture seule, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft.

Si vous déclarez une variable objet de type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), vous ne pourrez pas accéder à toutes les propriétés de l’objet [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) . Tandis que agent prend également en charge [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), cette dernière interface est fournie uniquement à des fins de compatibilité descendante et prend en charge uniquement les propriétés des versions précédentes.

-   [**Enabled**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Statu**](status-property.md)

 

 