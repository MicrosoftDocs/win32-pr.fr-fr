---
title: Implémentation du canal Client-Side
description: Implémentation du canal côté client dans l’appel de procédure distante (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840569"
---
# <a name="client-side-pipe-implementation"></a>Implémentation du canal Client-Side

L’application cliente doit implémenter les procédures suivantes, que le stub client appellera pendant le transfert de données :

-   Une procédure Pull (pour un canal d’entrée)
-   Procédure push (pour un canal de sortie)
-   Une procédure Alloc pour allouer une mémoire tampon pour les données de transfert

Toutes ces procédures doivent utiliser les arguments spécifiés par le fichier d’en-tête généré par MIDL. En outre, l’application cliente doit avoir une variable d’État pour identifier où localiser ou placer les données.

La procédure Alloc peut également être aussi simple ou complexe que nécessaire. Par exemple, il peut retourner un pointeur vers la même mémoire tampon chaque fois que le stub appelle la fonction, ou il peut allouer une quantité de mémoire différente à chaque fois. Si vos données sont déjà au format approprié (un tableau d’éléments de canal, par exemple), vous pouvez coordonner la procédure Alloc avec la procédure pull pour allouer une mémoire tampon qui contient déjà les données. Dans ce cas, votre procédure pull peut être une routine vide.

L’allocation de mémoire tampon doit être en octets. Les procédures push et pull, en revanche, manipulent les éléments dont la taille en octets dépend de la façon dont ils ont été définis.

Cette section décrit l’implémentation cliente des canaux d’entrée et de sortie dans les sections suivantes :

-   [Implémentation de canaux d’entrée sur le client](implementing-input-pipes-on-the-client.md)
-   [Implémentation de canaux de sortie sur le client](implementing-output-pipes-on-the-client.md)

 

 




