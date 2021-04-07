---
description: COM+ fournit un environnement de développement d’entreprise basé sur le modèle COM (Component Object Model) Microsoft, pour la création d’applications distribuées basées sur des composants.
ms.assetid: 141982d4-1e6c-4f01-8b0e-8b94f20dd82c
title: Vue d’ensemble de la programmation COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c225b5ebb6f04f74d6071dc0305d219993fa606e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748076"
---
# <a name="com-programming-overview"></a>Vue d’ensemble de la programmation COM+

COM+ fournit un environnement de développement d’entreprise basé sur le modèle COM (Component Object Model) Microsoft, pour la création d’applications distribuées basées sur des composants. Il fournit également les outils nécessaires pour créer des applications multicouches transactionnelles. COM+ associe des améliorations au développement COM traditionnel avec de nombreux services d’administration et de programmation utiles. Pour obtenir la liste complète de ces services, consultez [services com+](com--services.md) .

Les améliorations COM incluent les améliorations apportées aux threads et à la sécurité, ainsi que l’introduction des services de synchronisation. Les services incluent l’outil d’administration Services de composants.

Pour ceux qui connaissent la programmation COM, les améliorations de COM+ sont significatives, notamment les suivantes :

-   COM+ implémente un modèle de thread appelé thread cloisonné neutre, qui permet à un composant d’avoir un accès sérialisé, ainsi que la possibilité de s’exécuter sur n’importe quel thread.
-   COM+ prend en charge les composants avec un environnement spécial appelé [contexte](com--contexts.md), qui fournit un ensemble extensible de propriétés qui définissent l’environnement d’exécution du composant.
-   COM+ fournit la sécurité basée sur les rôles, l’exécution d’objets asynchrones et un moniker intégré qui représente une référence à une instance d’objet s’exécutant sur un serveur hors processus.

## <a name="application-and-component-administration"></a>Administration des applications et des composants

Dans COM+, une base de données d’inscription, nommée RegDB, stocke les métadonnées qui décrivent les composants. Cette base de données est hautement optimisée pour le type d’informations dont COM+ a besoin pour l’activation des composants et est utilisée à la place du Registre système. En outre, COM+ expose le *catalogue com+*, qui accède aux informations de RegDB. Le catalogue COM+ est un magasin de données système qui contient des informations de configuration pour les applications COM+ sur un ordinateur serveur donné.

Enfin, l’outil d’administration Services de composants fournit une interface utilisateur entièrement scriptable permettant aux développeurs et aux administrateurs d’administrer les composants, ainsi que de déployer des applications multicouches côté client et côté serveur. Pour plus d’informations, consultez [déploiement d’applications com+](deploying-com--applications.md).

## <a name="automatic-transactions"></a>Transactions automatiques

COM+ prend en charge toute la sémantique Microsoft Transaction Server (MTS) 2,0 et ajoute la fonctionnalité [automatique](enabling-auto-done-for-a-method.md) , que vous pouvez définir à l’aide de l’outil d’administration Services de composants. Cette fonctionnalité permet au système d’abandonner automatiquement une transaction si une exception est déclenchée ou de la valider si ce n’est pas le cas. Pour plus d’informations, consultez [transactions com+](com--transactions.md)et [activation juste-à-temps de com+](com--just-in-time-activation.md).

 

 



