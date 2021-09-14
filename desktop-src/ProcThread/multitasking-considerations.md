---
description: L’indication recommandée consiste à utiliser le moins de threads possible, ce qui réduit l’utilisation des ressources système.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Considérations relatives au multitâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324816"
---
# <a name="multitasking-considerations"></a>Considérations relatives au multitâche

L’indication recommandée consiste à utiliser le moins de threads possible, ce qui réduit l’utilisation des ressources système. Les performances en sont alors améliorées. Le multitâche a des besoins en ressources et des conflits potentiels à prendre en compte lors de la conception de votre application. Voici les exigences en matière de ressources :

-   Le système consomme de la mémoire pour les informations de contexte requises par les processus et les threads. Par conséquent, le nombre de processus et de threads pouvant être créés est limité par la mémoire disponible.
-   Le fait de suivre un grand nombre de threads consomme un temps processeur non négligeable. Si le nombre de threads est trop élevé, la plupart d’entre eux ne seront pas en mesure d’effectuer une progression significative. Si la majorité des threads en cours se trouvent dans un même processus, les threads des autres processus sont planifiés à une fréquence moindre.

L’accès partagé aux ressources risque de créer des conflits. Pour les éviter, vous devez synchroniser l’accès aux ressources partagées. Cela est vrai pour les ressources système (telles que les ports de communication), les ressources partagées par plusieurs processus (comme les descripteurs de fichiers) ou les ressources d’un processus unique (telles que les variables globales) accessibles par plusieurs threads. L’échec de la synchronisation de l’accès (dans le même processus ou dans des processus différents) peut entraîner des problèmes tels que les blocages et les conditions de concurrence. Objets et fonctions de synchronisation que vous pouvez utiliser pour coordonner le partage des ressources entre plusieurs threads. Pour plus d’informations sur la synchronisation, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md). La réduction du nombre de threads rend plus facile et plus efficace la synchronisation des ressources.

Le serveur de pipeline est une bonne conception pour une application multithread. Dans cette conception, vous créez un thread par processeur et les files d’attente de build des requêtes pour lesquelles l’application gère les informations de contexte. Un thread traiterait toutes les demandes dans une file d’attente avant le traitement des demandes dans la file d’attente suivante.

 

 



