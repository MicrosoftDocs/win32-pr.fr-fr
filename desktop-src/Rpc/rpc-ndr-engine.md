---
title: Moteur de NDR RPC (RPC)
description: Le moteur de représentation de données réseau (NDR) de l’appel de procédure distante (RPC) est le moteur de marshaling des composants RPC et DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0dd01ae40562528ac89c8b9dcfb0b9009ead5ca1a92b2cde90c3274d574fc1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018419"
---
# <a name="rpc-ndr-engine-rpc"></a>Moteur de NDR RPC (RPC)

Le moteur de représentation de données réseau (NDR) de l’appel de procédure distante (RPC) est le moteur de marshaling des composants RPC et DCOM. Le moteur de NDR gère tous les problèmes liés au stub d’un appel distant. En tant que processus, le marshaling de NDR est piloté par le code C des stubs générés par MIDL, un générateur de type JIT MIDL, ou par les stubs générés par d’autres outils ou écrits manuellement. À son tour, le moteur de rapport de non-remise pilote le temps d’exécution sous-jacent (DCOM ou RPC) qui communique avec des transports spécifiques.

Bien que les stubs soient du code C générés par MIDL, les applications sont invitées à traiter les stubs comme opaques, et fortement déconseillé de modifier quoi que ce soit dans le stub. Le comportement n’est pas défini si ces routines de NDR sont appelées hors contexte.

Le moteur de rapport de données RPC est décrit plus en détail dans les rubriques suivantes :

-   [Syntaxe de transfert et NDR64](transfer-syntax-and-ndr64.md)
-   [Chaînes de format de NDR RPC](rpc-ndr-format-strings.md)
-   [Référence de l’interface de NDR RPC](rpc-ndr-interface-reference.md)

 

 




