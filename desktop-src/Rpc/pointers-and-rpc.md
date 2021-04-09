---
title: Pointeurs et RPC
description: Il est très efficace d’utiliser des pointeurs en tant que paramètres de fonction C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840521"
---
# <a name="pointers-and-rpc"></a>Pointeurs et RPC

Il est très efficace d’utiliser des pointeurs en tant que paramètres de fonction C. Le pointeur ne coûte que quelques octets et peut être utilisé pour accéder à une grande quantité de mémoire. Toutefois, dans une application distribuée, les procédures du client et du serveur se trouvent dans des espaces d’adressage différents ; elles peuvent être sur des ordinateurs différents. Par conséquent, le client et le serveur n’ont généralement pas accès au même espace mémoire.

Quand l’un des paramètres de la procédure distante est un pointeur vers un objet, le client doit transmettre une copie de cet objet et de son pointeur au serveur. Si la procédure distante modifie l’objet par le biais de son pointeur, le serveur retourne le pointeur et sa copie modifiée.

MIDL offre des attributs de pointeur pour réduire la quantité de surcharge requise et la taille de votre application. Cette section traite de l’objectif et des utilisations des attributs de pointeur MIDL. Elle présente également des informations sur la gestion des pointeurs dans les applications RPC. Elle est composée des rubriques suivantes :

-   [Genres de pointeurs](kinds-of-pointers.md)
-   [Pointeurs et allocation de mémoire](pointers-and-memory-allocation.md)
-   [Types de pointeurs par défaut](default-pointer-types.md)
-   [Héritage de type d’attribut de pointeur](pointer-attribute-type-inheritance.md)

 

 




