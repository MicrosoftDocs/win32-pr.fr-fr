---
description: Création d’une application COM+
ms.assetid: eec4e871-36c2-4e60-9808-1400efcfc60c
title: Création d’une application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09eb296ad0a5f2326b5d931f59a5075d001d89f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516797"
---
# <a name="creating-a-new-com-application"></a><span data-ttu-id="190aa-103">Création d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="190aa-103">Creating a New COM+ Application</span></span>

<span data-ttu-id="190aa-104">La création d’une nouvelle application COM+ requiert deux étapes de base, comme suit :</span><span class="sxs-lookup"><span data-stu-id="190aa-104">Creating a new COM+ application requires two basic steps, as follows:</span></span>

-   <span data-ttu-id="190aa-105">Création d’une application COM+ vide (décrite ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="190aa-105">Creating an empty COM+ application (described below).</span></span>
-   <span data-ttu-id="190aa-106">Ajout de composants à l’application.</span><span class="sxs-lookup"><span data-stu-id="190aa-106">Adding components to the application.</span></span> <span data-ttu-id="190aa-107">(Voir [installation de nouveaux composants](installing-new-components.md) et [importation de composants](importing-components.md).)</span><span class="sxs-lookup"><span data-stu-id="190aa-107">(See [Installing New Components](installing-new-components.md) and [Importing Components](importing-components.md).)</span></span>

<span data-ttu-id="190aa-108">**Pour créer une application COM+ vide**</span><span class="sxs-lookup"><span data-stu-id="190aa-108">**To create an empty COM+ application**</span></span>

1.  <span data-ttu-id="190aa-109">Dans l’arborescence de la console de l’outil d’administration Services de composants, sélectionnez l’ordinateur sur lequel vous souhaitez créer une application.</span><span class="sxs-lookup"><span data-stu-id="190aa-109">In the console tree of the Component Services administrative tool, select the computer on which you want to create an application.</span></span>

2.  <span data-ttu-id="190aa-110">Sélectionnez le dossier **applications com+** pour cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="190aa-110">Select the **COM+ Applications** folder for that computer.</span></span>

3.  <span data-ttu-id="190aa-111">Dans le menu **action** , pointez sur **nouveau**, puis cliquez sur **application**.</span><span class="sxs-lookup"><span data-stu-id="190aa-111">On the **Action** menu, point to **New**, and then click **Application**.</span></span> <span data-ttu-id="190aa-112">Vous pouvez également cliquer avec le bouton droit sur le dossier **applications com+** , pointer sur **nouveau**, puis cliquer sur **application**.</span><span class="sxs-lookup"><span data-stu-id="190aa-112">You can also right-click the **COM+ Applications** folder, point to **New**, and then click **Application**.</span></span>

4.  <span data-ttu-id="190aa-113">Sur la page d' **Accueil** de l’Assistant Installation de l’application com+, cliquez sur **suivant**, puis dans la boîte de dialogue **installer ou créer une nouvelle application** , cliquez sur **créer une application vide**.</span><span class="sxs-lookup"><span data-stu-id="190aa-113">On the **Welcome** page of the COM+ Application Install Wizard, click **Next**, and then in the **Install or Create a New Application** dialog box, click **Create an empty application**.</span></span>

5.  <span data-ttu-id="190aa-114">Dans la zone prévue à cet effet, tapez un nom pour la nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="190aa-114">In the box provided, type a name for the new application.</span></span> <span data-ttu-id="190aa-115">(Notez que les caractères spéciaux suivants ne peuvent pas être utilisés dans un nom d’application : \\ ,/, ~, !, @, \# ,%, ^, &, \* , (,), \| ,}, {, \] , \[ , ', ", >, <,., ?, : et ;.) Sous **type d’activation**, cliquez sur application de **bibliothèque** ou **application serveur**.</span><span class="sxs-lookup"><span data-stu-id="190aa-115">(Note that the following special characters cannot be used in an application name: \\, /, ~, !, @, \#, %, ^, &, \*, (, ), \|, }, {, \], \[, ', ", >, <, ., ?, :, and ;.) Under **Activation type**, click **Library application** or **Server application**.</span></span> <span data-ttu-id="190aa-116">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="190aa-116">Click **Next**.</span></span>

    > [!Note]  
    > <span data-ttu-id="190aa-117">Une application serveur s’exécute dans son propre processus.</span><span class="sxs-lookup"><span data-stu-id="190aa-117">A server application runs in its own process.</span></span> <span data-ttu-id="190aa-118">Les applications serveur peuvent prendre en charge tous les services COM+.</span><span class="sxs-lookup"><span data-stu-id="190aa-118">Server applications can support all COM+ services.</span></span> <span data-ttu-id="190aa-119">Une application de bibliothèque s’exécute dans le processus du client qui la crée.</span><span class="sxs-lookup"><span data-stu-id="190aa-119">A library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="190aa-120">Les applications de bibliothèque peuvent utiliser la sécurité basée sur les rôles, mais ne prennent pas en charge l’accès à distance ou les composants en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="190aa-120">Library applications can use role-based security but do not support remote access or queued components.</span></span>

     

6.  <span data-ttu-id="190aa-121">Dans la boîte de dialogue **définir l’identité** de l’application, choisissez l’identité sous laquelle l’application s’exécutera.</span><span class="sxs-lookup"><span data-stu-id="190aa-121">In the **Set Application Identity** dialog box, choose an identity under which the application will run.</span></span> <span data-ttu-id="190aa-122">Si vous sélectionnez **cet utilisateur**, tapez le nom d’utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="190aa-122">If you select **This user**, type the user name and password.</span></span> <span data-ttu-id="190aa-123">Vous devez également retaper le mot de passe dans la zone **confirmer le mot de passe** .</span><span class="sxs-lookup"><span data-stu-id="190aa-123">You must also retype the password in the **Confirm password** box.</span></span> <span data-ttu-id="190aa-124">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="190aa-124">Click **Next**.</span></span> <span data-ttu-id="190aa-125">(La sélection par défaut pour l’identité de l’application est **utilisateur interactif**.</span><span class="sxs-lookup"><span data-stu-id="190aa-125">(The default selection for application identity is **Interactive User**.</span></span> <span data-ttu-id="190aa-126">L’utilisateur interactif est l’utilisateur connecté à l’ordinateur serveur à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="190aa-126">The interactive user is the user logged on to the server computer at any given time.</span></span> <span data-ttu-id="190aa-127">Vous pouvez sélectionner un autre utilisateur en sélectionnant **cet utilisateur** et en entrant un utilisateur ou un groupe spécifique.)</span><span class="sxs-lookup"><span data-stu-id="190aa-127">You can select a different user by selecting **This user** and entering a specific user or group.)</span></span>

    > [!Note]  
    > <span data-ttu-id="190aa-128">La boîte de dialogue **définir l’identité** de l’application s’affiche uniquement si vous avez sélectionné **application serveur** comme type d’activation de la nouvelle application dans la boîte de dialogue précédente de l’Assistant Installation de l’application com.</span><span class="sxs-lookup"><span data-stu-id="190aa-128">The **Set Application Identity** dialog box appears only if you selected **Server application** for the new application's activation type in the COM Application Install Wizard's preceding dialog box.</span></span> <span data-ttu-id="190aa-129">La propriété Identity n’est pas utilisée pour les applications de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="190aa-129">The identity property is not used for library applications.</span></span>

     

7.  <span data-ttu-id="190aa-130">Dans la boîte de dialogue **Ajouter des rôles d’application** , ajoutez tous les rôles que vous souhaitez associer à l’application.</span><span class="sxs-lookup"><span data-stu-id="190aa-130">In the **Add Application Roles** dialog box, add any roles you want to associate with the application.</span></span> <span data-ttu-id="190aa-131">Par défaut, seul le rôle **CreatorOwner** est défini.</span><span class="sxs-lookup"><span data-stu-id="190aa-131">By default, only the **CreatorOwner** role is defined.</span></span> <span data-ttu-id="190aa-132">Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="190aa-132">For information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

8.  <span data-ttu-id="190aa-133">Dans la boîte de dialogue **Ajouter des utilisateurs aux rôles** , remplissez chaque rôle que vous avez créé lors de la dernière étape avec les utilisateurs, les groupes ou les principaux de sécurité intégrés auxquels vous souhaitez accorder les privilèges associés à ce rôle.</span><span class="sxs-lookup"><span data-stu-id="190aa-133">In the **Add Users to Roles** dialog box, populate each role you created in the last step with the users, groups, or built-in security principals to which you want to grant the privileges associated with that role.</span></span> <span data-ttu-id="190aa-134">Par défaut, l’utilisateur interactif est placé dans le rôle **CreatorOwner** .</span><span class="sxs-lookup"><span data-stu-id="190aa-134">By default, the interactive user is placed in the **CreatorOwner** role.</span></span>

9.  <span data-ttu-id="190aa-135">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="190aa-135">Click **Finish**.</span></span>

<span data-ttu-id="190aa-136">La nouvelle application s’affiche désormais sous le dossier **applications com+** dans l’arborescence de la console de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="190aa-136">The new application will now be displayed under the **COM+ Applications** folder in the console tree of the Component Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="190aa-137">À compter de Windows Server 2003, les vérifications d’accès sont activées par défaut lors de la création d’une application COM+.</span><span class="sxs-lookup"><span data-stu-id="190aa-137">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="190aa-138">Dans les versions précédentes, les contrôles d’accès étaient désactivés par défaut au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="190aa-138">In previous versions, access checks were disabled by default at the application level.</span></span> <span data-ttu-id="190aa-139">Le résultat est que, par défaut, l’accès à une application COM+ est autorisé uniquement pour les utilisateurs qui se trouvent dans les rôles associés à l’application.</span><span class="sxs-lookup"><span data-stu-id="190aa-139">The result is that by default, access to a COM+ application is allowed only to users that are in the roles associated with the application.</span></span> <span data-ttu-id="190aa-140">(Voir [administration de la sécurité basée sur les rôles](role-based-security-administration.md).) Vous pouvez également autoriser l’accès à tous les utilisateurs en désactivant les vérifications d’accès sur une application COM+.</span><span class="sxs-lookup"><span data-stu-id="190aa-140">(See [Role-Based Security Administration](role-based-security-administration.md).) Alternatively, you can allow access to all users by disabling access checks on a COM+ application.</span></span> <span data-ttu-id="190aa-141">(Voir [activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md).)</span><span class="sxs-lookup"><span data-stu-id="190aa-141">(See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md).)</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="190aa-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="190aa-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="190aa-143">Copier des composants</span><span class="sxs-lookup"><span data-stu-id="190aa-143">Copying Components</span></span>](copying-components.md)
</dt> <dt>

[<span data-ttu-id="190aa-144">Suppression d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="190aa-144">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)
</dt> <dt>

[<span data-ttu-id="190aa-145">Importation de composants</span><span class="sxs-lookup"><span data-stu-id="190aa-145">Importing Components</span></span>](importing-components.md)
</dt> <dt>

[<span data-ttu-id="190aa-146">Installation de nouveaux composants</span><span class="sxs-lookup"><span data-stu-id="190aa-146">Installing New Components</span></span>](installing-new-components.md)
</dt> <dt>

[<span data-ttu-id="190aa-147">Déplacement des composants</span><span class="sxs-lookup"><span data-stu-id="190aa-147">Moving Components</span></span>](moving-components.md)
</dt> <dt>

[<span data-ttu-id="190aa-148">Suppression d’un composant d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="190aa-148">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)
</dt> </dl>

 

 



