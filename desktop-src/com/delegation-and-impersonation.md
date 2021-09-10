---
title: Délégation et emprunt d’identité
description: Dans les scénarios client/serveur, il est courant pour un serveur d’appeler un autre serveur pour accomplir une tâche au nom d’un client. La situation dans laquelle un serveur est autorisé à agir au nom d’un client est appelée délégation.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363399"
---
# <a name="delegation-and-impersonation"></a>Délégation et emprunt d’identité

Dans les scénarios client/serveur, il est courant pour un serveur d’appeler un autre serveur pour accomplir une tâche au nom d’un client. La situation dans laquelle un serveur est autorisé à agir au nom d’un client est appelée *délégation*.

Du point de vue de la sécurité, deux problèmes se posent concernant la délégation :

-   Que doit être autorisé le serveur lorsqu’il agit au nom du client ?
-   Quelle identité est présentée par le serveur lorsqu’il appelle d’autres serveurs pour le compte d’un client ?

Pour traiter ces problèmes, COM fournit les fonctionnalités suivantes. Le client peut définir un *niveau d’emprunt d’identité* qui détermine dans quelle mesure le serveur pourra agir en tant que client. Si le client accorde une autorité suffisante au serveur, le serveur peut *emprunter l’identité* du client (prétend être). Lorsque vous empruntez l’identité du client, le serveur est autorisé à accéder uniquement aux objets ou aux ressources que le client est autorisé à utiliser. Le serveur, agissant comme un client, peut également activer le *masquage* pour masquer sa propre identité et projeter l’identité du client dans les appels à d’autres composants com.

![Diagramme qui montre comment le serveur agissant en tant que client peut activer le masquage.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Prenons le scénario illustré dans la figure précédente, où A et B sont des processus sur un ordinateur différent de C. le processus A appelle B et B appelle C. le client A définit le niveau d’emprunt d’identité. B définit la fonctionnalité de voilage. Si un définit un niveau d’emprunt d’identité qui autorise l’emprunt d’identité, B peut emprunter l’identité d’un lors de l’appel de C en son nom. L’identité présentée au processus C sera l’identité de l’identité de l’une ou de l’identité de B, selon que le masquage a été activé ou non par B. Si le masquage est activé, l’identité présentée au processus C correspond à celle d’un. Si le masquage n’est pas activé, l’identité de B est présentée à C.

Pour plus d'informations, voir les rubriques suivantes :

-   [Emprunt d'identité](impersonation.md)
-   [Niveaux d’emprunt d’identité](impersonation-levels.md)
-   [Masquer](cloaking.md)

 

 




