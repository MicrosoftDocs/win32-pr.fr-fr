---
description: Conception pour le déploiement
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Conception pour le déploiement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852376"
---
# <a name="designing-for-deployment"></a>Conception pour le déploiement

La planification de l’étendue des applications COM+ est une tâche de conception importante que vous devez prendre en compte au début. Les systèmes distribués qui sont destinés à s’exécuter à l’aide de COM+ doivent être conçus pour le déploiement avec le moins de configurations individuelles et pour utiliser le plus efficacement chaque processus. Vous pouvez également utiliser des techniques qui vous permettront d’obtenir des performances optimales lors du déploiement d’une application COM+. (Pour plus d’informations, consultez [déploiement pour une communication plus rapide](deploying-for-faster-communication.md).)

Lorsqu’il est affiché avec l’outil d’administration Services de composants, chaque application COM+ apparaît sous la forme d’un dossier dans lequel les jeux de composants sont regroupés logiquement. Bien que vous puissiez déplacer des composants individuels entre des dossiers de **composants** d’application COM+ (en d’autres termes, d’une application à une autre), plusieurs services définis au niveau de l’application com+, tels que la sécurité, peuvent différer. Ces paramètres de service peuvent avoir une incidence sur la portabilité.

## <a name="a-com-server-application-defines-a-process-boundary"></a>Une application serveur COM+ définit une limite de processus

Lorsque vous créez une nouvelle application serveur COM+, vous définissez en fait une nouvelle limite de processus. (Notez l’exception pour les applications de bibliothèque expliquées ci-dessous.) Ce processus devient l’instance d’application de contrôle pour les composants contenus dans l’application COM+. Ces composants sont tous exécutés in-process dans une nouvelle instance du programme exécutable COM+ chaque fois qu’un programme appelle une application COM+ pour la première fois. Cela signifie que tous les composants dans le dossier des **composants** d’une application com+ donnée s’exécutent dans un espace de processus unique qui sert de serveur DCOM. Dans l’application COM+, COM+ gère la mémoire, la coordination avec le Distributed Transaction Coordinator (DTC), l’activation de l’instance du composant juste-à-temps, la détection et la récupération des incidents et la sécurité basée sur les rôles.

## <a name="calling-across-com-application-boundaries"></a>Appel à travers les limites d’application COM+

Étant donné que chaque application COM+ est normalement implémentée en tant qu’exécutable distinct, le fractionnement d’une application distribuée entre plusieurs applications COM+ présente des appels COM out-of-process lorsque les composants d’une application COM+ appellent les composants dans une autre application COM+. Cela introduit une dégradation des performances en raison de la charge supplémentaire qui consiste à marshaler les paramètres COM entre les processus.

> [!Note]  
> Il n’y a rien de mal par nature avec cette altération des performances ; il vous suffit de savoir qu’il va se produire. En fonction du temps de réponse requis, du nombre d’utilisateurs qui demanderont simultanément des services d’entreprise et de la charge de démarrage ajoutée que chaque composant ajoute à chaque application COM+, vous pouvez constater que l’impact sur les performances attribuable aux appels inter-applications est acceptable.

 

L’une des possibilités qui élimine la baisse des performances de l’appel entre les limites d’application COM+ consiste à marquer une application COM+ donnée comme une application de bibliothèque. Une application de bibliothèque COM+ s’exécute dans le processus du client qui la crée. Bien sûr, aucun gain de performance n’a un coût nul. Dans ce cas, le compromis implique les limitations des applications de bibliothèque COM+. Une application de bibliothèque peut utiliser la sécurité basée sur les rôles, mais elle ne peut pas prendre en charge les composants en file d’attente ou l’accès à distance.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déploiement pour une communication plus rapide](deploying-for-faster-communication.md)
</dt> <dt>

[Conception pour la disponibilité](designing-for-availability.md)
</dt> <dt>

[Conception pour l’évolutivité](designing-for-scalability.md)
</dt> <dt>

[Conception pour la sécurité](designing-for-security.md)
</dt> </dl>

 

 



