---
title: Le modèle RPC
description: l’appel de procédure distante (RPC) pour les langages de programmation C et C++ est conçu pour répondre aux besoins des développeurs qui travaillent sur la nouvelle génération de logiciels pour les systèmes d’exploitation Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Appel de procédure distante RPC, décrit, modèle RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4c21a9fbbff24f4aafe9bad67186b65f4e3411b507d07953e29f806c6ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019709"
---
# <a name="the-rpc-model"></a>Le modèle RPC

l’appel de procédure distante (RPC) pour les langages de programmation C et C++ est conçu pour répondre aux besoins des développeurs qui travaillent sur la nouvelle génération de logiciels pour les systèmes d’exploitation Windows.

RPC est un mécanisme de communication interprocessus (IPC) puissant, robuste, efficace et sécurisé qui permet l’échange de données et l’appel de fonctionnalités résidant dans un processus différent. Ce processus peut se trouver sur le même ordinateur, sur le réseau local ou sur Internet. Cette section décrit le modèle de programmation RPC et le modèle pour les systèmes distribués qui peuvent être implémentés à l’aide de RPC.

RPC prend entièrement en charge les Windows 64 bits. Il existe trois types de processus : les processus natifs 32 bits, les processus natifs de 64 bits et les processus 32 bits s’exécutant sous l’émulateur de processus 32 bits sur un système 64 bits (souvent appelé processus WOW64). Pour plus d’informations sur WOW64, consultez [exécution d’Applications 32 bits](/windows/desktop/WinProg64/running-32-bit-applications). À l’aide de RPC, les développeurs peuvent communiquer en toute transparence entre les différents types de processus ; RPC gère automatiquement les différences de processus en arrière-plan.

Le RPC a été initialement développé en tant qu’extension de l’appel RPC OSF. À l’exception de certaines de ses fonctionnalités avancées, RPC est interopérable avec les implémentations d’autres fournisseurs de RPC OSF.

Cette section fournit également une vue d’ensemble des composants RPC et de leur fonctionnement. Les informations sont présentées dans les rubriques suivantes :

-   [Le modèle de programmation](the-programming-model.md)
-   [Modèle pour les systèmes distribués](the-model-for-distributed-systems.md)
-   [Fonctionnement de RPC](how-rpc-works.md)
-   [Composants Microsoft RPC](microsoft-rpc-components.md)

 

 