---
title: Présentation de la gestion de la mémoire RPC
description: Présentation de la gestion de la mémoire de l’appel de procédure distante (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194143"
---
# <a name="introduction-to-rpc-memory-management"></a>Présentation de la gestion de la mémoire RPC

Dans le contexte de RPC, la gestion de la mémoire implique les opérations suivantes :

-   Allocation et libération de la mémoire nécessaire pour simuler un espace d’adressage conceptuel unique entre le client et le serveur dans les différents espaces d’adressage des threads du client et du serveur.
-   Détermination du composant logiciel responsable de la gestion de la mémoire : l’application ou le stub généré par MIDL.
-   Sélection des attributs MIDL qui affectent la gestion de la mémoire : attributs directionnels, attributs du pointeur, attributs du tableau et \[ [ \_ nombre d’octets](/windows/desktop/Midl/byte-count)des attributs ACF \] , \[ [allocation](/windows/desktop/Midl/allocate) \] et activation de l' \[ [ \_ allocation](/windows/desktop/Midl/enable-allocate) \] .

Lorsqu’un programme appelle une fonction ou une procédure dans son espace d’adressage, la gestion de la mémoire est plus simple que dans une application distribuée. Pour illustrer cela, le diagramme suivant illustre une arborescence binaire. Pour passer cette structure de données à une procédure dans son espace d’adressage, un programme passe simplement un pointeur vers la racine de l’arborescence.

![arborescence binaire, avec des pointeurs vers des données de structure hébergées à la racine de l’arborescence](images/bintree.png)

Les applications RPC client/serveur partagent des données entre deux espaces mémoire différents. Ces espaces mémoire peuvent se trouver ou non sur le même ordinateur. Dans les deux cas, le client et le serveur n’ont pas d’accès direct à l’espace mémoire de l’autre. RPC dépend de la capacité à simuler l’espace d’adressage du programme client dans l’espace d’adressage du programme serveur. Elle doit également retourner les données, y compris les données nouvelles et modifiées, du serveur à la mémoire du client.

Dans les cas tels que l’arborescence binaire représentée dans le diagramme précédent, il n’est pas suffisant de passer un pointeur vers le nœud racine à une procédure distante. Soit le programme, soit les stubs doivent transmettre l’intégralité de l’arborescence à l’espace d’adressage du serveur pour que la procédure distante fonctionne sur celle-ci.

 

 