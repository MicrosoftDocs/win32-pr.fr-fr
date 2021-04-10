---
description: Dans le gestionnaire d’autorisations, un objet IAzApplicationGroup représente un groupe d’utilisateurs. Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective.
ms.assetid: 13950da1-b04f-4346-b216-9713cbdcd5b5
title: Définition de groupes d’utilisateurs en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1b4931d3b35658539284305e98096d7ecfc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868441"
---
# <a name="defining-groups-of-users-in-c"></a><span data-ttu-id="84f60-104">Définition de groupes d’utilisateurs en C++</span><span class="sxs-lookup"><span data-stu-id="84f60-104">Defining Groups of Users in C++</span></span>

<span data-ttu-id="84f60-105">Dans le gestionnaire d’autorisations, un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) représente un groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="84f60-105">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="84f60-106">Les rôles peuvent ensuite être attribués à ce groupe d’utilisateurs de manière collective.</span><span class="sxs-lookup"><span data-stu-id="84f60-106">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="84f60-107">Un objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) peut également inclure d’autres objets **IAzApplicationGroup** en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="84f60-107">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="84f60-108">Pour plus d’informations sur les groupes d’applications, voir [utilisateurs et groupes](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="84f60-108">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="84f60-109">Un groupe peut être défini par des listes explicites de membres et de non-membres, ou par une requête LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="84f60-109">A group can be defined either by explicit lists of members and nonmembers, or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="84f60-110">Les exemples suivants montrent comment créer chaque type de groupe d’applications :</span><span class="sxs-lookup"><span data-stu-id="84f60-110">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="84f60-111">Création d’un groupe de base</span><span class="sxs-lookup"><span data-stu-id="84f60-111">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="84f60-112">Création d’un groupe de requêtes LDAP</span><span class="sxs-lookup"><span data-stu-id="84f60-112">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="84f60-113">Création d’un groupe de base</span><span class="sxs-lookup"><span data-stu-id="84f60-113">Creating a Basic Group</span></span>

<span data-ttu-id="84f60-114">Un groupe d’applications de base est défini par les membres inclus dans les propriétés des [**membres**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) et des non- [**membres**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) de l’objet [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) qui représente le groupe.</span><span class="sxs-lookup"><span data-stu-id="84f60-114">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="84f60-115">Les utilisateurs et les groupes répertoriés dans la propriété **membres** sont inclus dans le groupe d’applications, et les utilisateurs et les groupes répertoriés dans la propriété non- **membres** sont exclus du groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="84f60-115">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="84f60-116">La liste de la propriété des éléments qui n’est pas **membre** est remplacée par la liste dans la propriété **members** .</span><span class="sxs-lookup"><span data-stu-id="84f60-116">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="84f60-117">L’exemple suivant montre comment créer un groupe d’applications de base et ajouter tous les utilisateurs locaux en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="84f60-117">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="84f60-118">L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.</span><span class="sxs-lookup"><span data-stu-id="84f60-118">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR sidString = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Add well-known SID for all local users to the group.
    if (!(sidString = SysAllocString(L"S-1-2-0")))
        MyHandleError("Could not allocate SID string name");
    hr = pAppGroup->AddMember(sidString, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add member to group");

    //  Save changes to the store.
    pAppGroup->Submit(0, myVar);

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(sidString);
    VariantClear(&myVar);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="84f60-119">Création d’un groupe de requêtes LDAP</span><span class="sxs-lookup"><span data-stu-id="84f60-119">Creating an LDAP Query Group</span></span>

<span data-ttu-id="84f60-120">Un groupe de requêtes LDAP a une appartenance définie par la requête contenue dans la valeur de sa propriété [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="84f60-120">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="84f60-121">L’exemple suivant montre comment créer un groupe d’applications de requête LDAP et ajouter tous les utilisateurs en tant que membres de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="84f60-121">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="84f60-122">L’exemple suppose qu’il existe déjà un magasin de stratégies XML nommé MyStore.xml dans le répertoire racine du lecteur C.</span><span class="sxs-lookup"><span data-stu-id="84f60-122">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplicationGroup* pAppGroup = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR groupName = NULL;
    BSTR ldapString = NULL;

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    VARIANT myVar; 
    myVar.vt = VT_NULL;

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
   storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application group object.
    if (!(groupName = SysAllocString(L"Trusted Users3")))
        MyHandleError("Could not allocate group name string");
    hr = pStore->CreateApplicationGroup(groupName, myVar, &pAppGroup);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create application group.");

    //  Set the Type property to AZ_GROUPTYPE_LDAP_QUERY.
    hr = pAppGroup->put_Type(AZ_GROUPTYPE_LDAP_QUERY);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Error changing type to LDAP query");

    //  Add LDAP query for all users.
    if (!(ldapString =
   SysAllocString(L"(&(objectCategory=person)(objectClass=user))")))
        MyHandleError("Could not allocate LDAP query string");
    hr = pAppGroup->put_LdapQuery(ldapString);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add query to group");

    //  Save changes to the store.
    hr = pAppGroup->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save changes to store.");

    //  Clean up resources.
    pStore->Release();
    pAppGroup->Release();
    SysFreeString(storeName);
    SysFreeString(groupName);
    SysFreeString(ldapString);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
