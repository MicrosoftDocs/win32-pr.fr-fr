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
# <a name="assigning-a-user-account-or-group-to-a-role"></a><span data-ttu-id="7444b-103">Attribution d’un compte d’utilisateur ou d’un groupe à un rôle</span><span class="sxs-lookup"><span data-stu-id="7444b-103">Assigning a User Account or Group to a Role</span></span>

<span data-ttu-id="7444b-104">Vous pouvez utiliser l’outil d’administration Services de composants pour remplir un rôle avec des comptes d’utilisateur ou des groupes.</span><span class="sxs-lookup"><span data-stu-id="7444b-104">You can use the Component Services administrative tool to populate a role with user accounts or groups.</span></span> <span data-ttu-id="7444b-105">La méthode recommandée pour attribuer un compte d’utilisateur à un rôle consiste à affecter le compte d’utilisateur à un groupe, puis à attribuer le groupe au rôle.</span><span class="sxs-lookup"><span data-stu-id="7444b-105">The preferred way to assign a user account to a role is to assign the user account to a group and then assign the group to the role.</span></span> <span data-ttu-id="7444b-106">L’utilisation de groupes pour remplir des rôles vous permet de gérer plus facilement un grand nombre d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7444b-106">Using groups to populate roles makes it easier for you to manage large numbers of users.</span></span> <span data-ttu-id="7444b-107">Dans l’aide en ligne de l’outil d’administration gestion de l’ordinateur, consultez la rubrique « utilisateurs et groupes locaux » pour plus d’informations sur la création de groupes ou l’affectation d’un compte d’utilisateur à un groupe.</span><span class="sxs-lookup"><span data-stu-id="7444b-107">In the online help for the Computer Management administrative tool, see the topic "Local Users and Groups" for more information about creating groups or assigning a user account to a group.</span></span>

> [!Note]  
> <span data-ttu-id="7444b-108">Pour permettre aux utilisateurs réseau non authentifiés d’exécuter une application COM+, les rôles d’application doivent inclure l’utilisateur anonyme.</span><span class="sxs-lookup"><span data-stu-id="7444b-108">To allow unauthenticated network users to run a COM+ application, the application roles must include the Anonymous user.</span></span> <span data-ttu-id="7444b-109">À compter de Windows Server 2003, par défaut, l’utilisateur anonyme n’est pas inclus dans le groupe tout le monde.</span><span class="sxs-lookup"><span data-stu-id="7444b-109">Starting with Windows Server 2003, by default, the Anonymous user is not included in the Everyone group.</span></span>

 

<span data-ttu-id="7444b-110">Une fois que vous avez attribué le compte d’utilisateur au groupe Windows approprié, procédez comme suit pour attribuer le groupe Windows au rôle.</span><span class="sxs-lookup"><span data-stu-id="7444b-110">After you have assigned the user account to the appropriate Windows group, follow these steps to assign the Windows group to the role.</span></span>

<span data-ttu-id="7444b-111">**Pour affecter un groupe Windows à un rôle de sécurité**</span><span class="sxs-lookup"><span data-stu-id="7444b-111">**To assign a Windows group to a security role**</span></span>

1.  <span data-ttu-id="7444b-112">Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="7444b-112">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="7444b-113">Développez la vue dans l’arborescence de la console jusqu’à ce que les rôles de l’application soient visibles.</span><span class="sxs-lookup"><span data-stu-id="7444b-113">Expand the view in the console tree until the application's roles are visible.</span></span>

2.  <span data-ttu-id="7444b-114">Localisez le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="7444b-114">Locate the role to which you want to add the user account or group.</span></span>

    > [!Note]  
    > <span data-ttu-id="7444b-115">Si le rôle que vous recherchez ne figure pas dans le dossier **rôles** , le rôle n’a pas été ajouté à l’application.</span><span class="sxs-lookup"><span data-stu-id="7444b-115">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="7444b-116">Il doit être ajouté à l’application par le développeur avant que vous puissiez attribuer des comptes d’utilisateur au rôle.</span><span class="sxs-lookup"><span data-stu-id="7444b-116">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

     

3.  <span data-ttu-id="7444b-117">Cliquez avec le bouton droit sur le dossier **utilisateurs** dans le rôle, pointez sur **nouveau**, puis cliquez sur **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="7444b-117">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

4.  <span data-ttu-id="7444b-118">Dans le volet inférieur de la fenêtre **Sélectionner les utilisateurs ou les groupes** , tapez le nom complet de l’utilisateur ou du groupe que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="7444b-118">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="7444b-119">Si vous ne connaissez pas le nom, cliquez sur le bouton **avancé** , puis cliquez sur **Rechercher maintenant** pour afficher la liste des utilisateurs et des groupes dans le domaine sélectionné.</span><span class="sxs-lookup"><span data-stu-id="7444b-119">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="7444b-120">Sélectionnez un utilisateur ou un groupe dans la liste **nom (RDN)** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7444b-120">Select a user or group from the **Name (RDN)** list, and click **OK**.</span></span>

5.  <span data-ttu-id="7444b-121">Pour ajouter des comptes d’utilisateur ou des groupes supplémentaires, répétez l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="7444b-121">To add more user accounts or groups, repeat step 4.</span></span>

6.  <span data-ttu-id="7444b-122">Lorsque vous avez terminé d’ajouter des comptes et des groupes d’utilisateurs au rôle, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7444b-122">When you have finished adding user accounts and groups to the role, click **OK**.</span></span>

<span data-ttu-id="7444b-123">Pour chaque compte d’utilisateur ou groupe que vous avez affecté au rôle, une icône s’affiche dans le dossier **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="7444b-123">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span> <span data-ttu-id="7444b-124">La nouvelle appartenance au rôle prend effet lors du prochain démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="7444b-124">The new role membership takes effect the next time the application is started.</span></span>

 

 



