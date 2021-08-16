---
description: Les magasins de stratégies d’autorisation stockés dans Active Directory prennent en charge la délégation de l’administration.
ms.assetid: ccad4c19-7a16-4599-9a42-23cae7084418
title: Délégation de la définition des autorisations en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f79202a3f8ee21934f890d3c5a66a19be4466fa2b1ecdfe31672a4edfc2319e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782053"
---
# <a name="delegating-the-defining-of-permissions-in-c"></a>Délégation de la définition des autorisations en C++

Les magasins de stratégies d’autorisation stockés dans Active Directory prennent en charge la délégation de l’administration. L’administration peut être déléguée à des utilisateurs et à des groupes au niveau du magasin, de l’application ou de l’étendue.

À chaque niveau correspond une liste d’administrateurs et de lecteurs. Les administrateurs d’un magasin, d’une application ou d’une étendue peuvent lire et modifier le magasin de stratégies au niveau délégué. Les lecteurs peuvent lire le magasin de stratégies au niveau délégué, mais ne peuvent pas modifier le magasin.

Un utilisateur ou un groupe qui est soit un administrateur, soit un lecteur d’une application doit également être ajouté en tant qu’utilisateur délégué du magasin de stratégies qui contient cette application. De même, un utilisateur ou un groupe qui est un administrateur ou un lecteur d’étendue doit être ajouté en tant qu’utilisateur délégué de l’application qui contient cette étendue.

Par exemple, pour déléguer l’administration d’une étendue, ajoutez d’abord l’utilisateur ou le groupe à la liste des utilisateurs délégués du magasin qui contient l’étendue en appelant la méthode [**IAzAuthorizationStore :: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser) . Ajoutez ensuite l’utilisateur ou le groupe à la liste des utilisateurs délégués de l’application qui contient l’étendue en appelant la méthode [**IAzApplication :: AddDelegatedPolicyUser**](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser) . Enfin, ajoutez l’utilisateur ou le groupe à la liste des administrateurs de l’étendue en appelant la méthode [**IAzScope :: AddPolicyAdministrator**](/windows/desktop/api/Azroles/nf-azroles-iazscope-addpolicyadministrator) .

Les magasins de stratégies basés sur XML ne prennent pas en charge la délégation à un niveau quelconque.

Une étendue dans un magasin d’autorisations stocké dans Active Directory ne peut pas être déléguée si l’étendue contient des définitions de tâches qui incluent des règles d’autorisation ou des définitions de rôles qui incluent des règles d’autorisation.

L’exemple suivant montre comment déléguer l’administration d’une application. L’exemple suppose qu’il existe déjà un magasin de stratégies d’autorisation Active Directory à l’emplacement spécifié, que ce magasin de stratégies contient une application nommée Expense et que cette application ne contient pas de tâches avec des scripts de règle d’entreprise.


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



 

 



