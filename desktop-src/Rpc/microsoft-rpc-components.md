---
title: Composants RPC
description: Composants d’appel de procédure distante (RPC).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- Appel de procédure distante RPC, décrit, composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940018"
---
# <a name="rpc-components"></a>Composants RPC

RPC comprend les composants principaux suivants :

-   Compilateur MIDL
-   Bibliothèques Runtime et fichiers d’en-tête
-   Fournisseur de services de noms (parfois appelé Localisateur)
-   Mappeur de point de terminaison (parfois appelé mappeur de port)

Dans le modèle RPC, vous pouvez spécifier formellement une interface aux procédures distantes à l’aide d’un langage conçu à cet effet. Cette langue est appelée IDL (Interface Definition Language). L’implémentation Microsoft de ce langage est appelée Microsoft Interface Definition Language, ou MIDL.

Après avoir créé une interface, vous devez la passer par le compilateur MIDL. Ce compilateur génère les stubs qui traduisent les appels de procédure locale en appels de procédure distante. Les stubs sont des fonctions d’espace réservé qui effectuent des appels aux fonctions de la bibliothèque Runtime, qui gèrent l’appel de procédure distante. L’avantage de cette approche est que le réseau devient presque complètement transparent pour votre application distribuée. Votre programme client appelle ce qui semble être une procédure locale ; la tâche de les transformer en appels distants est effectuée automatiquement. Tout le code qui traduit des données, accède au réseau et récupère les résultats est généré pour vous par le compilateur MIDL et est invisible pour votre application.

 

 




