---
title: Conception d’interfaces accessibles à distance
description: Avec l’avènement du modèle d’objet de composant distribué, il est important que votre interface personnalisée soit accessible à distance, même si vous envisagez de l’utiliser uniquement dans le processus.
ms.assetid: 2ee4d950-dfd5-4965-bd77-a600e878be59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3502604d62e6a5129ca3e3538761722909c0198f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292782"
---
# <a name="designing-remotable-interfaces"></a>Conception d’interfaces accessibles à distance

Avec l’avènement du modèle d’objet de composant distribué, il est important que votre interface personnalisée soit accessible à distance, même si vous envisagez de l’utiliser uniquement dans le processus.

MIDL est plus qu’un simple moyen de générer des fichiers d’en-tête pour vos interfaces. Il s’agit d’un langage de programmation pour la communication à distance qui vous permet d’utiliser vos interfaces à travers les limites des ordinateurs, des processus et des threads. Cela signifie que vous devez vérifier le comportement de vos interfaces définies par MIDL dans ces conditions avant de publier votre programme pour les clients. Si vous avez commis une erreur dans votre IDL et que l’interface n’est pas correctement mise à distance, il peut être difficile de remédier à cette erreur. Vous devez modifier votre interface avec un nouvel IID et conserver l’ancienne dans pour des raisons de compatibilité descendante ou vous devez convertir chaque client et chaque ordinateur serveur en même temps.

Même si votre interface ne sera jamais utilisée hors processus, elle peut être utilisée sur plusieurs threads. Le pire problème pour un fichier IDL non vérifié peut survenir pour les serveurs in-process qui ne prennent pas en charge plusieurs [threads cloisonnés uniques](single-threaded-apartments.md). Un serveur qui ne spécifie pas de modèle de thread est implicitement monothread. Tout ce qui est marqué d’un thread unique est forcé sur le thread qui a d’abord appelé [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Si un autre thread était celui qui a activé l’objet, toutes les interfaces sur ce serveur à thread unique doivent être retransmises au thread d’activation, ce qui peut entraîner un retour de REGDB \_ E \_ IIDNOTREG en réponse à un appel à [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))). À moins que vous ne puissiez absolument affirmer que votre interface est à la fois en cours de traitement et qu’elle va toujours être appelée sur le même thread, vous obtiendrez à distance à un moment donné.

Enfin, en tant que concepteur d’interface, vous devez prendre en compte la façon dont les applications clientes utiliseront votre interface. Deux choses, ensemble, déterminent si une interface est efficace au-delà des limites de processus et de machine : la fréquence des appels de méthode à travers la limite de l’interface et la quantité de données à transférer dans un appel de méthode donné. Bien que COM rende les appels inter-processus et inter-réseaux transparents pour les programmes, il ne peut pas effectuer d’appels à fréquence élevée et à bande passante élevée efficacement dans les espaces d’adressage. Dans certains cas, il est plus approprié de concevoir des interfaces qui sont généralement implémentées uniquement comme serveurs in-process, tandis que les autres interfaces sont plus appropriées pour une utilisation à distance.

 

 




