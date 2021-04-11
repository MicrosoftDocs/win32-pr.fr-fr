---
description: Vous pouvez supprimer des comptes d’utilisateur ou des groupes d’un rôle lorsque les utilisateurs ou les membres des groupes ne doivent plus avoir accès aux ressources d’application auxquelles le rôle est attribué.
ms.assetid: d2cfa5cb-a143-41de-9aa2-7af7fce10ed7
title: Déplacement d’un compte d’utilisateur ou d’un groupe vers un autre rôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2401d792066212269d4eaa4eb11eadfef6e2d73e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111290"
---
# <a name="moving-a-user-account-or-group-to-a-different-role"></a><span data-ttu-id="1f3f5-103">Déplacement d’un compte d’utilisateur ou d’un groupe vers un autre rôle</span><span class="sxs-lookup"><span data-stu-id="1f3f5-103">Moving a User Account or Group to a Different Role</span></span>

<span data-ttu-id="1f3f5-104">Vous pouvez supprimer des comptes d’utilisateur ou des groupes d’un rôle lorsque les utilisateurs ou les membres des groupes ne doivent plus avoir accès aux ressources d’application auxquelles le rôle est attribué.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-104">You can remove user accounts or groups from a role when the users or members of the groups should no longer be given access to the application resources to which the role is assigned.</span></span>

<span data-ttu-id="1f3f5-105">**Pour supprimer un compte d’utilisateur ou un groupe d’un rôle**</span><span class="sxs-lookup"><span data-stu-id="1f3f5-105">**To remove a user account or group from a role**</span></span>

1.  <span data-ttu-id="1f3f5-106">Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le rôle qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-106">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the role you are interested in.</span></span> <span data-ttu-id="1f3f5-107">Développez la vue dans l’arborescence de la console jusqu’à ce que les utilisateurs du rôle soient visibles.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-107">Expand the view in the console tree until the users for the role are visible.</span></span>

2.  <span data-ttu-id="1f3f5-108">Cliquez avec le bouton droit sur le compte d’utilisateur ou le groupe que vous souhaitez supprimer, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-108">Right-click the user account or group you want to remove, and then click **Delete**.</span></span>

3.  <span data-ttu-id="1f3f5-109">Quand la boîte de dialogue **confirmer la suppression** de l’élément s’affiche, cliquez sur **Oui** pour supprimer le compte d’utilisateur ou le groupe.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-109">When prompted by the **Confirm Item Delete** dialog box, click **Yes** to delete the user account or group.</span></span>

<span data-ttu-id="1f3f5-110">Le compte d’utilisateur ou le groupe que vous avez supprimé du rôle ne s’affiche plus dans le dossier **utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="1f3f5-110">The user account or group that you have removed from the role no longer appears in the **Users** folder.</span></span> <span data-ttu-id="1f3f5-111">La nouvelle appartenance au rôle prend effet lors du prochain démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-111">The new role membership takes effect the next time the application is started.</span></span> <span data-ttu-id="1f3f5-112">Si vous avez apporté des modifications à l' **application système**, vous devez redémarrer l’ordinateur pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="1f3f5-112">If you have made changes to the **System Application**, you must restart the computer for the changes to take effect.</span></span>

 

 



