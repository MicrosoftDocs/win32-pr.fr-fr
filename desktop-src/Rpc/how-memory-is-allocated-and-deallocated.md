---
title: Comment la mémoire est allouée et désallouée
description: Par défaut, le code stub généré par le compilateur MIDL appelle des fonctions fournies par l’utilisateur pour allouer et libérer de la mémoire. Ces fonctions, nommées MIDL \_ utilisateur \_ allocate et MIDL \_ utilisateur \_ gratuit, doivent être fournies par le développeur et liées à l’application.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c32ac4d33fbd67f617f79125921ddfffc0de5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194220"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Comment la mémoire est allouée et désallouée

Par défaut, le code stub généré par le compilateur MIDL appelle des fonctions fournies par l’utilisateur pour allouer et libérer de la mémoire. Ces fonctions, nommées [**MIDL \_ utilisateur \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) et [**MIDL \_ utilisateur \_ gratuit**](/windows/desktop/Midl/midl-user-free-1), doivent être fournies par le développeur et liées à l’application.

Toutes les applications doivent fournir des implémentations de l' [**\_ \_ allocation utilisateur MIDL**](/windows/desktop/Midl/midl-user-allocate-1) et du [**MIDL \_ utilisateur \_ gratuit**](/windows/desktop/Midl/midl-user-free-1), même si les noms de ces fonctions peuvent ne pas apparaître explicitement dans les stubs. La seule exception est quand vous compilez en mode de compatibilité OSF (/OSF). Ces fonctions fournies par l’utilisateur doivent correspondre à un prototype de fonction défini spécifique, mais dans le cas contraire, elles peuvent être implémentées de quelque façon que ce soit, pratique ou utile pour l’application. Les applications peuvent également utiliser le package de gestion de mémoire RpcSs. La bibliothèque Runtime RPC Microsoft fournit ce groupe de fonctions.

Les sections suivantes décrivent les fonctions de gestion de la mémoire RPC.

-   [**allouer un \_ utilisateur MIDL \_**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**\_utilisateur \_ gratuit MIDL**](/windows/desktop/Midl/midl-user-free-1)
-   [Package de gestion de mémoire RpcSs](rpcss-memory-management-package.md)

 

 