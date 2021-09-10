---
title: Utilisation du substitut System-Supplied
description: Utilisation du substitut System-Supplied
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363579"
---
# <a name="using-the-system-supplied-surrogate"></a>Utilisation du substitut System-Supplied

Pour utiliser le substitut fourni par le système pour votre serveur DLL, inscrivez la DLL en spécifiant une chaîne vide ou une valeur **null** pour la valeur [DllSurrogate](dllsurrogate.md) dans le registre. Lorsqu’une demande d’activation pour un serveur de DLL désigné est fournie à COM, COM lance le processus de substitution par défaut et la DLL demandée (en spécifiant le CLSID sur la ligne de commande de lancement en interne) en même temps pour éviter un appel séparé. (Pour plus d’informations sur l’exécution de plusieurs serveurs DLL dans un processus de substitution, consultez [partage de substitution](surrogate-sharing.md).)

L’implémentation par défaut du processus de substitution est un serveur Pseudo-COM de style de modèle thread mixte. Lorsque plusieurs serveurs DLL sont chargés dans un seul processus de substitution, ce processus garantit que chaque serveur DLL est instancié à l’aide du modèle de thread spécifié dans le registre pour ce serveur. Tous les serveurs à thread libre chargés sont regroupés dans le cloisonnement multithread, tandis que chaque serveur à threads cloisonnés réside dans un cloisonnement monothread. Si un serveur DLL prend en charge les deux modèles de thread, COM choisit le multithreading.

Ce processus de substitution est écrit de sorte que COM gère à la fois le déchargement des serveurs DLL et l’arrêt du processus de substitution.

Le substitut fourni par le système fonctionne très bien pour la plupart des développeurs, et est très facile à utiliser. Toutefois, les développeurs qui ont des considérations spéciales peuvent décider qu’un substitut personnalisé est nécessaire. Pour plus d’informations, consultez [écriture d’un substitut personnalisé](writing-a-custom-surrogate.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Substituts de DLL](dll-surrogates.md)
</dt> </dl>

 

 




