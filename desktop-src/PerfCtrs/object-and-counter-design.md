---
description: Un objet de performance est une entité pour laquelle les données de performances sont disponibles.
ms.assetid: 97b9c9ec-e758-4928-b3fa-90d220bca5fb
title: Conception d’objets et de compteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9556882f5dd6c323697d9d41fa80727895550a5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007182"
---
# <a name="object-and-counter-design"></a>Conception d’objets et de compteurs

Un objet de performance est une entité pour laquelle les données de performances sont disponibles. Les compteurs de performances définissent le type de données disponibles pour un objet de performance. Une application peut fournir des informations pour plusieurs objets de performance. Les objets de performance peuvent contenir des compteurs d’instance unique ou des compteurs à instances multiples. Un objet d’instance unique retourne un ensemble unique de valeurs de compteur.

Un objet à instances multiples retourne une instance de l’objet pour chaque occurrence de l’objet que l’application contrôle. Par exemple, une application SCSI peut définir un objet lecteur avec deux compteurs, tels que les octets lus et les octets écrits. Lorsque le consommateur interroge l’objet, la DLL de performance retourne une instance de l’objet pour chaque lecteur que l’application contrôle.

Après avoir décidé si votre objet prend en charge une seule instance ou plusieurs instances, vous devez choisir le type de compteurs que vous souhaitez donner à l’objet. Par exemple, vous pouvez fournir des valeurs de compteur qui s’affichent sous forme de valeurs brutes, de taux ou de pourcentages.

pour obtenir la liste des types de compteurs prédéfinis que vous devez choisir, consultez la section types de compteurs du [Kit de déploiement Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)). Selon le type de compteur, vous pouvez simplement fournir les données brutes, ou vous devrez peut-être également fournir des informations de temps et de fréquence et des données de compteur supplémentaires utilisées par le consommateur pour calculer une valeur affichable.

La méthode que vous utilisez pour collecter les données peut être aussi simple que l’incrémentation d’un compteur chaque fois qu’une routine particulière de l’application est appelée, ou il peut impliquer des calculs longs. Les compteurs et les minuteurs doivent s’incrémenter et ne jamais être effacés. Les compteurs peuvent être encapsulés, à condition qu’ils ne soient pas encapsulés deux fois par le consommateur. Votre application peut collecter et stocker des données pendant leur exécution normale, à condition qu’elles n’affectent pas ses performances.

Pour certains types de données, il peut être plus efficace ou plus approprié de collecter les données à la demande. Dans ce cas, la DLL de performance doit communiquer à l’application que les données ont été demandées. Pour les données coûteuses à collecter (en termes de temps processeur ou d’utilisation de la mémoire), envisagez de collecter des données uniquement lorsque le consommateur demande des données **coûteuses** . Cela permet à un consommateur de demander régulièrement des données pour tous les compteurs qui ne sont pas coûteux. Les données peuvent être demandées uniquement lorsque cela est nécessaire. L’outil performance ne collecte pas de données **coûteuses** .

 

 
