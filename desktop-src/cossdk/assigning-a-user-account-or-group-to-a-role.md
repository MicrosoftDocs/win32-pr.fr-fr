---
description: Vous pouvez utiliser l’outil d’administration Services de composants pour remplir un rôle avec des comptes d’utilisateur ou des groupes.
ms.assetid: 1cf7dc38-185a-4cc4-8f4c-44b6af4c5f4a
title: Attribution d’un compte d’utilisateur ou d’un groupe à un rôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53b37c9f0265e02c7abdf74eeaf81bd0b12e3d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517414"
---
# <a name="assigning-a-user-account-or-group-to-a-role"></a>Attribution d’un compte d’utilisateur ou d’un groupe à un rôle

Vous pouvez utiliser l’outil d’administration Services de composants pour remplir un rôle avec des comptes d’utilisateur ou des groupes. La méthode recommandée pour attribuer un compte d’utilisateur à un rôle consiste à affecter le compte d’utilisateur à un groupe, puis à attribuer le groupe au rôle. L’utilisation de groupes pour remplir des rôles vous permet de gérer plus facilement un grand nombre d’utilisateurs. Dans l’aide en ligne de l’outil d’administration gestion de l’ordinateur, consultez la rubrique « utilisateurs et groupes locaux » pour plus d’informations sur la création de groupes ou l’affectation d’un compte d’utilisateur à un groupe.

> [!Note]  
> Pour permettre aux utilisateurs réseau non authentifiés d’exécuter une application COM+, les rôles d’application doivent inclure l’utilisateur anonyme. À compter de Windows Server 2003, par défaut, l’utilisateur anonyme n’est pas inclus dans le groupe tout le monde.

 

Une fois que vous avez attribué le compte d’utilisateur au groupe Windows approprié, procédez comme suit pour attribuer le groupe Windows au rôle.

**Pour affecter un groupe Windows à un rôle de sécurité**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe. Développez la vue dans l’arborescence de la console jusqu’à ce que les rôles de l’application soient visibles.

2.  Localisez le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe.

    > [!Note]  
    > Si le rôle que vous recherchez ne figure pas dans le dossier **rôles** , le rôle n’a pas été ajouté à l’application. Il doit être ajouté à l’application par le développeur avant que vous puissiez attribuer des comptes d’utilisateur au rôle.

     

3.  Cliquez avec le bouton droit sur le dossier **utilisateurs** dans le rôle, pointez sur **nouveau**, puis cliquez sur **utilisateur**.

4.  Dans le volet inférieur de la fenêtre **Sélectionner les utilisateurs ou les groupes** , tapez le nom complet de l’utilisateur ou du groupe que vous souhaitez ajouter. Si vous ne connaissez pas le nom, cliquez sur le bouton **avancé** , puis cliquez sur **Rechercher maintenant** pour afficher la liste des utilisateurs et des groupes dans le domaine sélectionné. Sélectionnez un utilisateur ou un groupe dans la liste **nom (RDN)** , puis cliquez sur **OK**.

5.  Pour ajouter des comptes d’utilisateur ou des groupes supplémentaires, répétez l’étape 4.

6.  Lorsque vous avez terminé d’ajouter des comptes et des groupes d’utilisateurs au rôle, cliquez sur **OK**.

Pour chaque compte d’utilisateur ou groupe que vous avez affecté au rôle, une icône s’affiche dans le dossier **utilisateurs** . La nouvelle appartenance au rôle prend effet lors du prochain démarrage de l’application.

 

 



