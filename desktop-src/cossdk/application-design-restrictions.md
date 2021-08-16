---
description: Certaines applications sont conçues d’une manière qui empêche l’installation de plusieurs instances de l’application sur un ordinateur.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restrictions relatives à la conception d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b98e7b7d8dddf1cd74224573d355e1f42d75c8ae6122d20977bbc1b38ffb99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917543"
---
# <a name="application-design-restrictions"></a>Restrictions relatives à la conception d’applications

Certaines applications sont conçues d’une manière qui empêche l’installation de plusieurs instances de l’application sur un ordinateur. Avec une telle limitation, une application ne peut pas utiliser la fonctionnalité de partitions. Vous devrez peut-être modifier les fonctionnalités de conception d’application suivantes pour que les partitions puissent être utilisées pour cette application.

## <a name="tables-and-arrays"></a>Tables et tableaux

Certaines applications créent des tables de base de données, des tables en mémoire ou des tableaux qui utilisent un CLSID comme clé de Registre unique. Sur un ordinateur sans partitions, cette clé de Registre est généralement ordinateur/CLSID (un CLSID par ordinateur).

À l’inverse, sur un ordinateur avec des partitions, cette clé de Registre est ID d’ordinateur/partition/ID d’application/CLSID (plusieurs instances d’un CLSID par ordinateur). Étant donné que la fonctionnalité partitions permet à plusieurs instances d’un CLSID d’exister sur un ordinateur, les applications qui contiennent des éléments de conception qui requièrent un CLSID unique par ordinateur peuvent être affectées.

## <a name="global-resources"></a>Ressources globales

Certaines applications utilisent des ressources globales, telles que la mémoire partagée, les fichiers de données et les entrées de registre. Cela peut entraîner des problèmes si plusieurs instances d’une telle application s’exécutent simultanément.

Par exemple, si un composant utilise de la mémoire partagée pour interagir avec d’autres composants, le composant doit être modifié afin que chaque instance du composant alloue sa propre mémoire partagée.

## <a name="type-libraries"></a>Bibliothèques de types

Les bibliothèques de types fournissent des informations sur les interfaces et les méthodes d’un composant. Ces informations sont utilisées à plusieurs fins, notamment les suivantes :

-   Marshaling de données entre des composants lorsque des appels de fonction sont effectués
-   Assistance des composants COM+ mis en file d’attente et des services d’événements COM+
-   fournir les informations correctes dans un éditeur de Visual Basic Microsoft

Les références à une bibliothèque de types sont installées dans le registre d’un ordinateur. Lorsque vous développez des applications qui seront appelées à partir de partitions, il est important que la dernière version d’une bibliothèque de types soit installée dans le registre. cela permet de s’assurer que l’éditeur de Visual Basic est utilisé pour obtenir des informations précises sur les méthodes disponibles pour ce composant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Composants et partitions COM+ en file d’attente](com--queued-components-and-partitions.md)
</dt> <dt>

[Implémentation de la partition](partition-implementation.md)
</dt> <dt>

[Inscription et activation de composants dans des partitions](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Que sont les partitions COM+ ?](what-are-com--partitions-.md)
</dt> </dl>

 

 



