---
description: Lors du développement d’applications COM+, les principales tâches incluent la conception de composants COM pour encapsuler la logique d’application et l’intégration de ces composants dans une application COM+, la création de l’application COM+ et l’administration de l’application par le biais du déploiement et de la maintenance.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Développement d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523244"
---
# <a name="developing-com-applications"></a>Développement d’applications COM+

Lors du développement d’applications COM+, les principales tâches incluent la conception de composants COM pour encapsuler la logique d’application et l’intégration de ces composants dans une application COM+, la création de l’application COM+ et l’administration de l’application par le biais du déploiement et de la maintenance.

## <a name="designing-com-components"></a>Conception de composants COM

Les étapes suivantes décrivent une procédure générale pour une bonne conception de composant :

1.  Définissez les classes COM et les classes d’implémentation.
2.  Regroupez les classes en composants.
3.  Sélectionnez l’ensemble des services COM+ pour votre composant, même si vous ne les spécifiez pas tous lors du développement du composant. Ces services peuvent être spécifiés ultérieurement à l’aide de l’outil d’administration Services de composants ou du modèle objet d’administration COM+ (pour plus d’informations sur le modèle objet d’administration COM+, consultez automatisation de l' [administration com+](automating-com--administration.md) ).

## <a name="creating-the-com-application"></a>Création de l’application COM+

Après avoir conçu les composants COM, le développeur intègre les composants dans une application COM+ et configure l’application. Les étapes suivantes décrivent le processus :

1.  Intégrez les composants dans une application COM+. Vous pouvez intégrer les composants à une application COM+ existante ou créer une nouvelle application (vide) pour les composants. (Consultez [création d’applications com+](creating-com--applications.md).)
2.  Spécifiez le jeu d’attributs approprié pour chacune des classes (le cas échéant) et, s’il n’est pas spécifié dans l’outil de développement. Ces attributs expriment les dépendances des composants sur les services COM+ sur lesquels l’implémentation peut s’appuyer (par exemple, les transactions, les composants en file d’attente, la sécurité, le regroupement d’objets et l’activation juste-à-temps).
3.  Configurez l’infrastructure de sécurité (rôles et attribution de rôles aux classes, interfaces et méthodes).
4.  Configurez des attributs spécifiques à l’environnement sur des classes et des applications (par exemple, la taille du pool d’objets par défaut). Ces attributs spécifiques à l’environnement peuvent être définis (ou modifiés) ultérieurement par l’administrateur système.
5.  Exportez l’application pour la redistribution et le déploiement.

Pour plus d’informations sur les étapes de la conception d’applications distribuées, consultez [conception d’applications com+](designing-com--applications.md).

## <a name="administering-com-applications"></a>Administration des applications COM+

En général, un développeur remet une application COM+ partiellement configurée à l’administrateur système. L’administrateur peut ensuite personnaliser l’application pour un ou plusieurs environnements spécifiques (par exemple, en ajoutant des comptes d’utilisateur dans des rôles et des noms de serveurs dans un cluster d’applications). Les tâches de l’administrateur sont les suivantes :

-   Installation de l’application COM+ partiellement configurée sur un ordinateur d’administration.
-   Fournir des attributs spécifiques à l’environnement, tels que les membres du rôle et la taille du pool d’objets.
-   Réexportation de l’application COM+ entièrement configurée.
-   Création d’un proxy d’application (si l’application doit être accessible à distance).

Une fois qu’une application est entièrement configurée pour un environnement spécifique, l’administrateur peut la déployer sur des ordinateurs de test ou de production. Cela implique l’installation de l’application COM+ entièrement configurée sur un ou plusieurs ordinateurs.

Pour plus d’informations sur les procédures d’administration COM+, consultez l’outil d’administration Services de composants.

 

 



