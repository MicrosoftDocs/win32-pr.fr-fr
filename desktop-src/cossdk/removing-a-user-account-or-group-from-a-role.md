---
description: Si un utilisateur modifie des privilèges ou si des rôles sont ajoutés à une application, vous pouvez déplacer un compte d’un rôle à un autre.
ms.assetid: 2d81a45a-9762-48b9-8395-3c3a4dcd5e8c
title: Suppression d’un compte d’utilisateur ou d’un groupe d’un rôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176272aef16af0d0a65d90f6a1d7628a5af232fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514950"
---
# <a name="removing-a-user-account-or-group-from-a-role"></a><span data-ttu-id="70349-103">Suppression d’un compte d’utilisateur ou d’un groupe d’un rôle</span><span class="sxs-lookup"><span data-stu-id="70349-103">Removing a User Account or Group from a Role</span></span>

<span data-ttu-id="70349-104">Si les privilèges d’un utilisateur changent ou si des rôles sont ajoutés à une application, vous pouvez déplacer un compte d’un rôle à un autre.</span><span class="sxs-lookup"><span data-stu-id="70349-104">If a user's privileges change or if roles are added to an application, you can move an account from one role to another role.</span></span> <span data-ttu-id="70349-105">Pour déplacer un compte d’utilisateur ou un groupe d’utilisateurs d’un rôle à un autre, vous devez supprimer le compte d’utilisateur ou le groupe de son rôle actuel, puis l’affecter au nouveau rôle.</span><span class="sxs-lookup"><span data-stu-id="70349-105">To move a user account or group of users from one role to another, you must remove the user account or group from its current role and then assign it to the new role.</span></span>

<span data-ttu-id="70349-106">**Pour déplacer un compte d’utilisateur ou un groupe d’un rôle à un autre**</span><span class="sxs-lookup"><span data-stu-id="70349-106">**To move a user account or group from one role to another**</span></span>

1.  <span data-ttu-id="70349-107">Supprimez le compte d’utilisateur ou le groupe du rôle auquel il ne doit plus appartenir, comme suit :</span><span class="sxs-lookup"><span data-stu-id="70349-107">Remove the user account or group from the role that it should no longer belong to, as follows:</span></span>

    1.  <span data-ttu-id="70349-108">Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="70349-108">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="70349-109">Développez la vue dans l’arborescence de la console jusqu’à ce que les utilisateurs du rôle soient visibles.</span><span class="sxs-lookup"><span data-stu-id="70349-109">Expand the view in the console tree until the users for the role are visible.</span></span>

    2.  <span data-ttu-id="70349-110">Cliquez avec le bouton droit sur le compte d’utilisateur ou le groupe que vous souhaitez supprimer, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="70349-110">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

    3.  <span data-ttu-id="70349-111">Quand la boîte de dialogue **confirmer la suppression** de l’élément s’affiche, cliquez sur **Oui** pour supprimer le compte d’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="70349-111">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

    <span data-ttu-id="70349-112">Le compte d’utilisateur ou le groupe que vous avez supprimé du rôle ne s’affiche plus dans le dossier **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="70349-112">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span>

2.  <span data-ttu-id="70349-113">Affectez le compte d’utilisateur ou le groupe que vous avez supprimé aux rôles auxquels l’utilisateur ou le groupe doit être affecté, comme suit :</span><span class="sxs-lookup"><span data-stu-id="70349-113">Assign the user account or group you have removed to the roles that the user or group should be assigned to, as follows:</span></span>

    1.  <span data-ttu-id="70349-114">Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="70349-114">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role to which you want to add the user account or group.</span></span> <span data-ttu-id="70349-115">Développez la vue dans l’arborescence de la console jusqu’à ce que les rôles de l’application soient visibles.</span><span class="sxs-lookup"><span data-stu-id="70349-115">Expand the view in the console tree until the application's roles are visible.</span></span>

    2.  <span data-ttu-id="70349-116">Localisez le rôle auquel vous souhaitez ajouter le compte d’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="70349-116">Locate the role to which you want to add the user account or group.</span></span>

        > [!Note]  
        > <span data-ttu-id="70349-117">Si le rôle que vous recherchez ne figure pas dans le dossier **rôles** , le rôle n’a pas été ajouté à l’application.</span><span class="sxs-lookup"><span data-stu-id="70349-117">If the role you are looking for is not in the **Roles** folder, the role has not been added to the application.</span></span> <span data-ttu-id="70349-118">Il doit être ajouté à l’application par le développeur avant que vous puissiez attribuer des comptes d’utilisateur au rôle.</span><span class="sxs-lookup"><span data-stu-id="70349-118">It must be added to the application by the developer before you can assign user accounts to the role.</span></span>

         

    3.  <span data-ttu-id="70349-119">Cliquez avec le bouton droit sur le dossier **utilisateurs** dans le rôle, pointez sur **nouveau**, puis cliquez sur **utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="70349-119">Right-click the **Users** folder in the role, point to **New**, and then click **User**.</span></span>

    4.  <span data-ttu-id="70349-120">Dans le volet inférieur de la fenêtre **Sélectionner les utilisateurs ou les groupes** , tapez le nom complet de l’utilisateur ou du groupe que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="70349-120">In the **Select Users or Groups** window, in the bottom pane, type the fully qualified name of the user or group you want to add.</span></span> <span data-ttu-id="70349-121">Si vous ne connaissez pas le nom, cliquez sur le bouton **avancé** , puis cliquez sur **Rechercher maintenant** pour afficher la liste des utilisateurs et des groupes dans le domaine sélectionné.</span><span class="sxs-lookup"><span data-stu-id="70349-121">If you do not know the name, click the **Advanced** button and then click **Find Now** to view a list of users and groups in the selected domain.</span></span> <span data-ttu-id="70349-122">Sélectionnez un utilisateur ou un groupe dans la liste **nom (RDN)** , puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="70349-122">Select a user or group from the **Name (RDN)** list and click **OK**.</span></span>

    5.  <span data-ttu-id="70349-123">Lorsque vous avez terminé d’ajouter le compte d’utilisateur ou le groupe au rôle, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="70349-123">When you have finished adding the user account or group to the role, click **OK**.</span></span>

    <span data-ttu-id="70349-124">Pour chaque compte d’utilisateur ou groupe que vous avez affecté au rôle, une icône s’affiche dans le dossier **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="70349-124">For each user account or group you have assigned to the role, an icon appears in the **Users** folder.</span></span>

<span data-ttu-id="70349-125">L’appartenance au rôle modifié pour le compte d’utilisateur ou le groupe prend effet lors du prochain démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="70349-125">The changed role membership for the user account or group takes effect the next time the application is started.</span></span>

 

 



