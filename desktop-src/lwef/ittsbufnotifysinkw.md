---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940266"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Le moteur doit appeler par **signet**. Lors du prétraitement de la sortie vocale, le code Microsoft Agent insère les signets entre les « mots » et utilise l’arrivée de ces signets pour piloter le texte dans la bulle. Alors que SAPI ne nécessite rien de plus que l’arrivée de ces signets à un moment donné avant la fin de l’énoncé, les signets doivent être retournés de façon relativement opportune pour prendre en charge Microsoft Agent.

Notez qu’il n’existe pas de concept strict de « Word » dans certains langages, tels que le japonais. La méthode [**Speak**](speak-method.md) de Microsoft Agent définit un « mot » comme une chaîne connectée de symboles qui a une signification et une prononciation en isolation. Microsoft Agent utilise un code d’analyse relativement simple pour déterminer ce qu’est un « mot » : il recherche les symboles séparés par un espace blanc. Par conséquent, il y a trois « mots » dans la chaîne anglaise « the 101 Dalmatians » : « The », « 101 » et « Dalmatians ». Le texte inclus dans la balise de la carte de l’agent Microsoft est traité comme un « mot » unique à des fins d’affichage.

 

 




