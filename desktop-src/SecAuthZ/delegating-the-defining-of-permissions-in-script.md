---
description: Vous pouvez déléguer l’administration des magasins de stratégies d’autorisation stockés dans Active Directory.
ms.assetid: a7b43dfe-f03e-4795-bbd3-746eb3449fd0
title: Délégation de la définition des autorisations dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9569f82271642a610919db8246cc6389daba309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319598"
---
# <a name="delegating-the-defining-of-permissions-in-script"></a><span data-ttu-id="2f4c6-103">Délégation de la définition des autorisations dans le script</span><span class="sxs-lookup"><span data-stu-id="2f4c6-103">Delegating the Defining of Permissions in Script</span></span>

<span data-ttu-id="2f4c6-104">Vous pouvez déléguer l’administration des magasins de stratégies d’autorisation stockés dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-104">You can delegate the administration of authorization policy stores that are stored in Active Directory.</span></span> <span data-ttu-id="2f4c6-105">L’administration peut être déléguée à des utilisateurs et à des groupes au niveau du magasin, de l’application ou de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="2f4c6-106">À chaque niveau correspond une liste d’administrateurs et de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="2f4c6-107">Les administrateurs d’un magasin, d’une application ou d’une étendue peuvent lire et modifier le magasin de stratégies au niveau délégué.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="2f4c6-108">Les lecteurs peuvent lire le magasin de stratégies au niveau délégué, mais ne peuvent pas modifier le magasin.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="2f4c6-109">Un utilisateur ou un groupe qui est soit un administrateur, soit un lecteur d’une application doit également être ajouté en tant qu’utilisateur délégué du magasin de stratégies qui contient cette application.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="2f4c6-110">De même, un utilisateur ou un groupe qui est un administrateur ou un lecteur d’étendue doit être ajouté en tant qu’utilisateur délégué de l’application qui contient cette étendue.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="2f4c6-111">**Pour déléguer l’administration d’une étendue**</span><span class="sxs-lookup"><span data-stu-id="2f4c6-111">**To delegate administration of a scope**</span></span>

1.  <span data-ttu-id="2f4c6-112">Ajoutez l’utilisateur ou le groupe à la liste des utilisateurs délégués du magasin qui contient l’étendue en appelant la méthode [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) de l’objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui contient l’étendue.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-112">Add the user or group to the list of delegated users of the store that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method of the [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that contains the scope.</span></span>
2.  <span data-ttu-id="2f4c6-113">Ajoutez l’utilisateur ou le groupe à la liste des utilisateurs délégués de l’application qui contient l’étendue en appelant la méthode [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) de l’objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) qui contient l’étendue.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-113">Add the user or group to the list of delegated users of the application that contains the scope by calling the [**AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method of the [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that contains the scope.</span></span>
3.  <span data-ttu-id="2f4c6-114">Ajoutez l’utilisateur ou le groupe à la liste des administrateurs de l’étendue en appelant la méthode [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) de l’objet [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="2f4c6-114">Add the user or group to the list of administrators of the scope by calling the [**AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method of the [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

> [!Note]  
> <span data-ttu-id="2f4c6-115">Les magasins de stratégies basés sur XML ne prennent pas en charge la délégation à un niveau quelconque.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-115">XML-based policy stores do not support delegation at any level.</span></span>

 

<span data-ttu-id="2f4c6-116">Si une étendue dans un magasin d’autorisations qui est stocké dans Active Directory contient des définitions de tâches qui incluent des règles d’autorisation ou des définitions de rôles qui incluent des règles d’autorisation, l’étendue ne peut pas être déléguée.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-116">If a scope within an authorization store that is stored in Active Directory contains task definitions that include authorization rules or role definitions that include authorization rules, the scope cannot be delegated.</span></span>

<span data-ttu-id="2f4c6-117">L’exemple suivant montre comment déléguer l’administration d’une application.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-117">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="2f4c6-118">L’exemple suppose qu’il existe déjà un magasin de stratégies d’autorisation Active Directory à l’emplacement spécifié, que ce magasin de stratégies contient une application nommée Expense et que cette application ne contient pas de tâches avec des scripts de règle d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2f4c6-118">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, _
    "msldap://CN=MyStore,CN=Program Data,DC=authmanager,DC=com"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Add a delegated policy user to the store.
AzManStore.AddDelegatedPolicyUserName("ExampleDomain\\UserName")

'  Add the user as an administrator of the application.
expenseApp.AddPolicyAdministratorName("ExampleDomain\\UserName")

'  Save changes to the store.
AzManStore.Submit
```



 

 



