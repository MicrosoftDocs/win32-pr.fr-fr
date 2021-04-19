---
description: Les magasins de stratégies d’autorisation stockés dans Active Directory prennent en charge la délégation de l’administration.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Délégation de la définition des autorisations en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc299e3506300da1f0db2b4a9bacfce60def1c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521881"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a><span data-ttu-id="7eb46-103">Délégation de la définition des autorisations en C++</span><span class="sxs-lookup"><span data-stu-id="7eb46-103">Delegating the Defining of Permissions in C++</span></span>

<span data-ttu-id="7eb46-104">Les magasins de stratégies d’autorisation stockés dans Active Directory prennent en charge la délégation de l’administration.</span><span class="sxs-lookup"><span data-stu-id="7eb46-104">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="7eb46-105">L’administration peut être déléguée à des utilisateurs et à des groupes au niveau du magasin, de l’application ou de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="7eb46-105">Administration can be delegated to users and groups at the store, application, or scope level.</span></span>

<span data-ttu-id="7eb46-106">À chaque niveau correspond une liste d’administrateurs et de lecteurs.</span><span class="sxs-lookup"><span data-stu-id="7eb46-106">At each level, there is a list of administrators and readers.</span></span> <span data-ttu-id="7eb46-107">Les administrateurs d’un magasin, d’une application ou d’une étendue peuvent lire et modifier le magasin de stratégies au niveau délégué.</span><span class="sxs-lookup"><span data-stu-id="7eb46-107">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="7eb46-108">Les lecteurs peuvent lire le magasin de stratégies au niveau délégué, mais ne peuvent pas modifier le magasin.</span><span class="sxs-lookup"><span data-stu-id="7eb46-108">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

<span data-ttu-id="7eb46-109">Un utilisateur ou un groupe qui est soit un administrateur, soit un lecteur d’une application doit également être ajouté en tant qu’utilisateur délégué du magasin de stratégies qui contient cette application.</span><span class="sxs-lookup"><span data-stu-id="7eb46-109">A user or group that is either an administrator or a reader of an application must also be added as a delegated user of the policy store that contains that application.</span></span> <span data-ttu-id="7eb46-110">De même, un utilisateur ou un groupe qui est un administrateur ou un lecteur d’étendue doit être ajouté en tant qu’utilisateur délégué de l’application qui contient cette étendue.</span><span class="sxs-lookup"><span data-stu-id="7eb46-110">Similarly, a user or group that is an administrator or a reader of a scope must be added as a delegated user of the application that contains that scope.</span></span>

<span data-ttu-id="7eb46-111">Par exemple, pour déléguer l’administration d’une étendue, ajoutez d’abord l’utilisateur ou le groupe à la liste des utilisateurs délégués du magasin qui contient l’étendue en appelant la méthode [**IAzAuthorizationStore :: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="7eb46-111">For example, to delegate administration of a scope, first add the user or group to the list of delegated users of the store that contains the scope by calling the [**IAzAuthorizationStore::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="7eb46-112">Ajoutez ensuite l’utilisateur ou le groupe à la liste des utilisateurs délégués de l’application qui contient l’étendue en appelant la méthode [**IAzApplication :: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) .</span><span class="sxs-lookup"><span data-stu-id="7eb46-112">Then add the user or group to the list of delegated users of the application that contains the scope by calling the [**IAzApplication::AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) method.</span></span> <span data-ttu-id="7eb46-113">Enfin, ajoutez l’utilisateur ou le groupe à la liste des administrateurs de l’étendue en appelant la méthode [**IAzScope :: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .</span><span class="sxs-lookup"><span data-stu-id="7eb46-113">Finally, add the user or group to the list of administrators of the scope by calling the [**IAzScope::AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) method.</span></span>

<span data-ttu-id="7eb46-114">Les magasins de stratégies basés sur XML ne prennent pas en charge la délégation à un niveau quelconque.</span><span class="sxs-lookup"><span data-stu-id="7eb46-114">XML-based policy stores do not support delegation at any level.</span></span>

<span data-ttu-id="7eb46-115">Une étendue dans un magasin d’autorisations stocké dans Active Directory ne peut pas être déléguée si l’étendue contient des définitions de tâches qui incluent des règles d’autorisation ou des définitions de rôles qui incluent des règles d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="7eb46-115">A scope within an authorization store that is stored in Active Directory cannot be delegated if the scope contains task definitions that include authorization rules or role definitions that include authorization rules.</span></span>

<span data-ttu-id="7eb46-116">L’exemple suivant montre comment déléguer l’administration d’une application.</span><span class="sxs-lookup"><span data-stu-id="7eb46-116">The following example shows how to delegate administration of an application.</span></span> <span data-ttu-id="7eb46-117">L’exemple suppose qu’il existe déjà un magasin de stratégies d’autorisation Active Directory à l’emplacement spécifié, que ce magasin de stratégies contient une application nommée Expense et que cette application ne contient pas de tâches avec des scripts de règle d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="7eb46-117">The example assumes that there is an existing Active Directory authorization policy store at the specified location, that this policy store contains an application named Expense, and that this application contains no tasks with business rule scripts.</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void)
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR userName = NULL;
    VARIANT myVar;
    
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
    myVar.vt = VT_NULL;

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize
   (AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Add a delegated policy user to the store.
    if (!(userName = SysAllocString(L"ExampleDomain\\UserName")))
        MyHandleError("Could not allocate username string.");
    hr = pStore->AddDelegatedPolicyUserName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to store as delegated policy user.");

    //  Add the user as an administrator of the application.
    hr = pApp->AddPolicyAdministratorName(userName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError
   ("Could not add user to application as administrator.");

    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(userName);
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



 

 



