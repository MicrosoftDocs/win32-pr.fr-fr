---
description: Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications. Les informations incluent les applications, les opérations, les tâches, les utilisateurs et les groupes d’utilisateurs associés au magasin.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Création d’un objet du magasin de stratégies d’autorisation en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be0b39633eb773b84ad16098f24b59cb23e5d9cc234afdfca414e9cba7a640b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782464"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a>Création d’un objet du magasin de stratégies d’autorisation en C++

Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications. Les informations incluent les applications, les opérations, les tâches, les utilisateurs et les groupes d’utilisateurs associés au magasin. Lorsqu’une application qui utilise le gestionnaire d’autorisations initialise, elle charge ces informations à partir du magasin. Le magasin de stratégies d’autorisation doit se trouver sur un système approuvé, car les administrateurs de ce système disposent d’un haut niveau d’accès au magasin.

Le gestionnaire d’autorisations prend en charge le stockage de la stratégie d’autorisation dans le service d’annuaire Active Directory ou dans un fichier XML, comme indiqué dans les exemples suivants. Dans l’API du gestionnaire d’autorisations, un magasin de stratégies d’autorisation est représenté par un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . Les exemples montrent comment créer un objet **AzAuthorizationStore** pour un magasin de Active Directory et un magasin XML.

-   [Création d’un magasin de Active Directory](#creating-an-active-directory-store)
-   [création d’un magasin de SQL Server](#creating-a-sql-server-store)
-   [Création d’un magasin XML](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a>Création d’un magasin de Active Directory

pour utiliser Active Directory pour stocker la stratégie d’autorisation, le domaine doit être au niveau fonctionnel du domaine **Windows Server 2003** . Le magasin de stratégies d’autorisation ne peut pas être situé dans un **contexte d’attribution de noms sans domaine** (également appelé partition d’application). Il est recommandé de placer le magasin dans le conteneur de **données de programme** sous une nouvelle unité d’organisation créée spécifiquement pour le magasin de stratégies d’autorisation. Il est également recommandé de placer le magasin dans le même réseau local que les serveurs d’applications qui exécutent des applications qui utilisent le Windows Store.

L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans Active Directory. L’exemple suppose qu’il existe déjà une Active Directory unité d’organisation nommée Program Data dans un domaine nommé authmanager.com.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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
    
    //  Create a null VARIANT for function parameters.
    VARIANT myVar;
    VariantInit(&myVar);

    //  Allocate a string for the distinguished name of the
 //  Active Directory store.
    if(!(storeName = SysAllocString
   (L"msldap://CN=MyAzStore,CN=Program Data,DC=authmanager,DC=com")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in Active Directory. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    VariantClear(&myVar);
    SysFreeString(storeName);
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



## <a name="creating-a-sql-server-store"></a>création d’un magasin de SQL Server

le gestionnaire d’autorisations prend en charge la création d’un magasin de stratégies d’autorisation basé sur Microsoft SQL Server. pour créer un magasin d’autorisations basé sur SQL Server, utilisez une URL qui commence par le préfixe **MSSQL://**. l’URL doit contenir une chaîne de connexion SQL valide, un nom de base de données et le nom du magasin de stratégies d’autorisation : **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.

si l’instance de SQL Server ne contient pas la base de données du gestionnaire d’autorisations spécifiée, le gestionnaire d’autorisations crée une nouvelle base de données portant ce nom.

> [!Note]  
> les connexions à un magasin de SQL Server ne sont pas chiffrées, sauf si vous configurez explicitement SQL le chiffrement pour la connexion ou configurez le chiffrement du trafic réseau qui utilise le protocole IPsec (Internet Protocol Security).

 

l’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans une base de données SQL Server.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the SQL Server store.
    if(!(storeName = SysAllocString
   (L"MSSQL://Driver={SQL Server};Server={AzServer};/AzDB/MyStore")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



## <a name="creating-an-xml-store"></a>Création d’un magasin XML

Le gestionnaire d’autorisations prend en charge la création d’un magasin de stratégies d’autorisation au format XML. Le magasin XML peut se trouver sur le même ordinateur que celui où l’application s’exécute, ou il peut être stocké à distance. La modification directe du fichier XML n’est pas prise en charge. Utilisez le composant logiciel enfichable MMC du gestionnaire d’autorisations ou l’API du gestionnaire d’autorisations pour modifier le magasin de stratégies.

Le gestionnaire d’autorisations ne prend pas en charge la délégation de l’administration d’un magasin de stratégies XML. Pour plus d’informations sur la délégation, consultez délégation [de la définition des autorisations en C++](delegating-the-defining-of-permissions-in-c--.md).

L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans un fichier XML.


```C++
#pragma comment(lib, "duser.lib")

#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;

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

    //  Allocate a string for the distinguished name of the XML store.
    if(!(storeName = SysAllocString(L"msxml://C:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store in an XML file. Use the
 //  AZ_AZSTORE_FLAG_CREATE flag.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_CREATE, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Call the submit method to save changes to the new store.
    hr = pStore->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save data to the store.");

    //  Clean up resources.
    pStore->Release();
    SysFreeString(storeName);
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



 

 



