---
description: Un objet IAzApplicationGroup représente un groupe d’utilisateurs. Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective. Un objet IAzApplicationGroup peut également inclure d’autres objets IAzApplicationGroup en tant que membres.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Définition de groupes d’utilisateurs dans le script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320550"
---
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="4e6b2-105">Définition de groupes d’utilisateurs dans le script</span><span class="sxs-lookup"><span data-stu-id="4e6b2-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="4e6b2-106">Dans le gestionnaire d’autorisations, un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) représente un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="4e6b2-107">Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="4e6b2-108">Un objet **IAzApplicationGroup** peut également inclure d’autres objets **IAzApplicationGroup** en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="4e6b2-109">Pour plus d’informations sur les groupes d’applications, voir [utilisateurs et groupes](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="4e6b2-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="4e6b2-110">Un groupe peut être défini à l’aide de listes explicites de membres et de non-membres ou d’une requête LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="4e6b2-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="4e6b2-111">Les exemples suivants montrent comment créer chaque type de groupe d’applications :</span><span class="sxs-lookup"><span data-stu-id="4e6b2-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="4e6b2-112">Création d’un groupe de base</span><span class="sxs-lookup"><span data-stu-id="4e6b2-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="4e6b2-113">Création d’un groupe de requêtes LDAP</span><span class="sxs-lookup"><span data-stu-id="4e6b2-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="4e6b2-114">Création d’un groupe de base</span><span class="sxs-lookup"><span data-stu-id="4e6b2-114">Creating a Basic Group</span></span>

<span data-ttu-id="4e6b2-115">Un groupe d’applications de base est défini par les membres inclus dans les propriétés des [**membres**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) et des non- [**membres**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) de l’objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) qui représente le groupe.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="4e6b2-116">Les utilisateurs et les groupes répertoriés dans la propriété **membres** sont inclus dans le groupe d’applications, et les utilisateurs et les groupes répertoriés dans la propriété non- **membres** sont exclus du groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="4e6b2-117">La liste de la propriété des éléments qui n’est pas **membre** est remplacée par la liste dans la propriété **members** .</span><span class="sxs-lookup"><span data-stu-id="4e6b2-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="4e6b2-118">L’exemple suivant montre comment créer un groupe d’applications de base et ajouter tous les utilisateurs locaux en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="4e6b2-119">L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="4e6b2-120">Création d’un groupe de requêtes LDAP</span><span class="sxs-lookup"><span data-stu-id="4e6b2-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="4e6b2-121">Un groupe de requêtes LDAP a une appartenance définie par la requête contenue dans la valeur de sa propriété [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="4e6b2-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="4e6b2-122">L’exemple suivant montre comment créer un groupe d’applications de requête LDAP et ajouter tous les utilisateurs en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="4e6b2-123">L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.</span><span class="sxs-lookup"><span data-stu-id="4e6b2-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
