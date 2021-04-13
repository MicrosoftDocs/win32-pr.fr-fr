---
title: Canaux (RPC)
description: Le constructeur de type pipe est un mécanisme très efficace pour la transmission de grandes quantités de données, ou toute quantité de données qui ne sont pas toutes disponibles en mémoire à un moment donné.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Appel de procédure distante RPC, décrit, canaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464079"
---
# <a name="pipes-rpc"></a>Canaux (RPC)

Le constructeur de type pipe est un mécanisme très efficace pour la transmission de grandes quantités de données, ou toute quantité de données qui ne sont pas toutes disponibles en mémoire à un moment donné. À l’aide d’un canal, le temps d’exécution RPC gère le transfert de données réel, éliminant la surcharge associée aux appels de procédure distante répétés.

Après qu’un client a appelé une procédure distante qui a un paramètre de canal, le client et le serveur entrent des boucles pour transférer des données. Les données peuvent être produites sur le client ou sur le serveur. Dans les deux cas, la quantité de données (en octets) n’a pas besoin d’être connue à l’avance. Les données peuvent être produites ou consommées de manière incrémentielle. Pendant la boucle de transfert de données, le serveur appelle des routines de stub qui chargent ou déchargent une mémoire tampon de données. Le client appelle des procédures définies par le programmeur pour allouer des tampons, charger des données dans les mémoires tampons et les décharger.

Cette section fournit une vue d’ensemble de l’utilisation de canaux pour les appels de procédure distante. Il présente la vue d’ensemble des rubriques suivantes :

-   [Terminologie des canaux essentiels](essential-pipe-terminology.md)
-   [État du canal](the-pipe-state.md)
-   [Définition de canaux dans des fichiers IDL](defining-pipes-in-idl-files.md)
-   [Implémentation de canal côté client](client-side-pipe-implementation.md)
-   [Implémentation de canal côté serveur](server-side-pipe-implementation.md)
-   [Règles pour plusieurs canaux](rules-for-multiple-pipes.md)
-   [Combinaison de paramètres de canal et de pas de canal](combining-pipe-and-nonpipe-parameters.md)

Pour plus d’informations sur la syntaxe et les restrictions des canaux, consultez [canal](/windows/desktop/Midl/pipe) dans la référence du langage MIDL. L’exemple de programme PIPES dans le kit de développement logiciel (SDK) samples du kit de développement logiciel (SDK) fournit des exemples d' \\ utilisation **\[ de dans, des canaux out \]** pour transférer des données entre un client et un serveur.

 

 
