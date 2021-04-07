---
title: Objet SpeechInput
description: Objet SpeechInput
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940118"
---
# <a name="the-speechinput-object"></a>Objet SpeechInput

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

L’objet [**SpeechInput**](https://www.bing.com/search?q=**SpeechInput**) fournit l’accès aux propriétés d’entrée vocale gérées par le serveur de l’agent. Les propriétés sont en lecture seule pour les applications clientes, mais l’utilisateur peut les modifier dans la feuille de propriétés de l’agent Microsoft. Le serveur retourne des valeurs uniquement si un moteur de reconnaissance vocale compatible a été installé et est activé.

Le [**moteur**](https://www.bing.com/search?q=**Engine**), les propriétés [**installées**](https://www.bing.com/search?q=**Installed**)et la [**langue**](https://www.bing.com/search?q=**Language**) ne sont plus prises en charge, mais (pour la compatibilité descendante) retournent des valeurs NULL si elles sont interrogées. Pour interroger ou définir le mode d’une reconnaissance vocale, utilisez la propriété [**SRModeID**](srmodeid-property.md) .

-   [Propriétés SpeechInput](speechinput-properties.md)

 

 




