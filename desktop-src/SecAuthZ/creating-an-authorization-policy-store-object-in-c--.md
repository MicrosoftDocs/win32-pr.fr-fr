---
description: Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications. Les informations incluent les applications, les opérations, les tâches, les utilisateurs et les groupes d’utilisateurs associés au magasin.
ms.assetid: 6fc84944-8050-4000-8856-36558d94e2fd
title: Création d’un objet du magasin de stratégies d’autorisation en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b50bfa4234f5adaf162b1499f85785a7d65f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951463"
---
# <a name="creating-an-authorization-policy-store-object-in-c"></a><span data-ttu-id="70010-104">Création d’un objet du magasin de stratégies d’autorisation en C++</span><span class="sxs-lookup"><span data-stu-id="70010-104">Creating an Authorization Policy Store Object in C++</span></span>

<span data-ttu-id="70010-105">Un magasin de stratégies d’autorisation contient des informations sur la stratégie de sécurité d’une application ou d’un groupe d’applications.</span><span class="sxs-lookup"><span data-stu-id="70010-105">An authorization policy store contains information about the security policy of an application or group of applications.</span></span> <span data-ttu-id="70010-106">Les informations incluent les applications, les opérations, les tâches, les utilisateurs et les groupes d’utilisateurs associés au magasin.</span><span class="sxs-lookup"><span data-stu-id="70010-106">The information includes the applications, operations, tasks, users, and groups of users associated with the store.</span></span> <span data-ttu-id="70010-107">Lorsqu’une application qui utilise le gestionnaire d’autorisations initialise, elle charge ces informations à partir du magasin.</span><span class="sxs-lookup"><span data-stu-id="70010-107">When an application that uses Authorization Manager initializes, it loads this information from the store.</span></span> <span data-ttu-id="70010-108">Le magasin de stratégies d’autorisation doit se trouver sur un système approuvé, car les administrateurs de ce système disposent d’un haut niveau d’accès au magasin.</span><span class="sxs-lookup"><span data-stu-id="70010-108">The authorization policy store must be located on a trusted system because administrators on that system have a high degree of access to the store.</span></span>

<span data-ttu-id="70010-109">Le gestionnaire d’autorisations prend en charge le stockage de la stratégie d’autorisation dans le service d’annuaire Active Directory ou dans un fichier XML, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="70010-109">Authorization Manager supports storing authorization policy either in the Active Directory directory service or in an XML file as shown in the following examples.</span></span> <span data-ttu-id="70010-110">Dans l’API du gestionnaire d’autorisations, un magasin de stratégies d’autorisation est représenté par un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="70010-110">In the Authorization Manager API, an authorization policy store is represented by an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="70010-111">Les exemples montrent comment créer un objet **AzAuthorizationStore** pour un magasin de Active Directory et un magasin XML.</span><span class="sxs-lookup"><span data-stu-id="70010-111">The examples show how to create an **AzAuthorizationStore** object for an Active Directory store and an XML store.</span></span>

-   [<span data-ttu-id="70010-112">Création d’un magasin de Active Directory</span><span class="sxs-lookup"><span data-stu-id="70010-112">Creating an Active Directory Store</span></span>](#creating-an-active-directory-store)
-   [<span data-ttu-id="70010-113">Création d’un magasin de SQL Server</span><span class="sxs-lookup"><span data-stu-id="70010-113">Creating a SQL Server Store</span></span>](#creating-a-sql-server-store)
-   [<span data-ttu-id="70010-114">Création d’un magasin XML</span><span class="sxs-lookup"><span data-stu-id="70010-114">Creating an XML Store</span></span>](#creating-an-xml-store)

## <a name="creating-an-active-directory-store"></a><span data-ttu-id="70010-115">Création d’un magasin de Active Directory</span><span class="sxs-lookup"><span data-stu-id="70010-115">Creating an Active Directory Store</span></span>

<span data-ttu-id="70010-116">Pour utiliser Active Directory pour stocker la stratégie d’autorisation, le domaine doit être au niveau fonctionnel de domaine **Windows Server 2003** .</span><span class="sxs-lookup"><span data-stu-id="70010-116">To use Active Directory to store the authorization policy, the domain must be in the **Windows Server 2003** domain functional level.</span></span> <span data-ttu-id="70010-117">Le magasin de stratégies d’autorisation ne peut pas être situé dans un **contexte d’attribution de noms sans domaine** (également appelé partition d’application).</span><span class="sxs-lookup"><span data-stu-id="70010-117">The authorization policy store cannot be located in a **Non-Domain Naming Context** (also called an application partition).</span></span> <span data-ttu-id="70010-118">Il est recommandé de placer le magasin dans le conteneur de **données de programme** sous une nouvelle unité d’organisation créée spécifiquement pour le magasin de stratégies d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="70010-118">It is recommended that the store be located in the **Program Data** container under a new organizational unit created specifically for the authorization policy store.</span></span> <span data-ttu-id="70010-119">Il est également recommandé de placer le magasin dans le même réseau local que les serveurs d’applications qui exécutent des applications qui utilisent le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="70010-119">It is also recommended that the store be located within the same local area network as application servers that run applications that use the store.</span></span>

<span data-ttu-id="70010-120">L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="70010-120">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in Active Directory.</span></span> <span data-ttu-id="70010-121">L’exemple suppose qu’il existe déjà une Active Directory unité d’organisation nommée Program Data dans un domaine nommé authmanager.com.</span><span class="sxs-lookup"><span data-stu-id="70010-121">The example assumes that there is an existing Active Directory organizational unit named Program Data in a domain named authmanager.com.</span></span>


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



## <a name="creating-a-sql-server-store"></a><span data-ttu-id="70010-122">Création d’un magasin de SQL Server</span><span class="sxs-lookup"><span data-stu-id="70010-122">Creating a SQL Server Store</span></span>

<span data-ttu-id="70010-123">Le gestionnaire d’autorisations prend en charge la création d’un magasin de stratégies d’autorisation basé sur Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70010-123">Authorization Manager supports creating a Microsoft SQL Server–based authorization policy store.</span></span> <span data-ttu-id="70010-124">Pour créer un magasin d’autorisations basé sur SQL Server, utilisez une URL qui commence par le préfixe **MSSQL://**.</span><span class="sxs-lookup"><span data-stu-id="70010-124">To create a SQL Server–based authorization store, use a URL that begins with the prefix **MSSQL://**.</span></span> <span data-ttu-id="70010-125">L’URL doit contenir une chaîne de connexion SQL valide, un nom de base de données et le nom du magasin de stratégies d’autorisation : **MSSQL://**_ConnectionString_ *_/_* _DatabaseName_ *_/_* _PolicyStoreName_.</span><span class="sxs-lookup"><span data-stu-id="70010-125">The URL must contain a valid SQL connection string, a database name, and the name of the authorization policy store: **MSSQL://**_ConnectionString_*_/_*_DatabaseName_*_/_*_PolicyStoreName_.</span></span>

<span data-ttu-id="70010-126">Si l’instance de SQL Server ne contient pas la base de données du gestionnaire d’autorisations spécifiée, le gestionnaire d’autorisations crée une nouvelle base de données portant ce nom.</span><span class="sxs-lookup"><span data-stu-id="70010-126">If the instance of SQL Server does not contain the specified Authorization Manager database, Authorization Manager creates a new database with that name.</span></span>

> [!Note]  
> <span data-ttu-id="70010-127">Les connexions à un magasin de SQL Server ne sont pas chiffrées, sauf si vous configurez explicitement le chiffrement SQL pour la connexion ou si vous configurez le chiffrement du trafic réseau qui utilise le protocole IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="70010-127">Connections to a SQL Server store are not encrypted unless you explicitly set up SQL encryption for the connection or set up encryption of the network traffic that uses Internet Protocol Security (IPsec).</span></span>

 

<span data-ttu-id="70010-128">L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans une base de données SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70010-128">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in a SQL Server database.</span></span>


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



## <a name="creating-an-xml-store"></a><span data-ttu-id="70010-129">Création d’un magasin XML</span><span class="sxs-lookup"><span data-stu-id="70010-129">Creating an XML Store</span></span>

<span data-ttu-id="70010-130">Le gestionnaire d’autorisations prend en charge la création d’un magasin de stratégies d’autorisation au format XML.</span><span class="sxs-lookup"><span data-stu-id="70010-130">Authorization Manager supports creating an authorization policy store in XML format.</span></span> <span data-ttu-id="70010-131">Le magasin XML peut se trouver sur le même ordinateur que celui où l’application s’exécute, ou il peut être stocké à distance.</span><span class="sxs-lookup"><span data-stu-id="70010-131">The XML store can be located on the same computer where the application runs, or it can be stored remotely.</span></span> <span data-ttu-id="70010-132">La modification directe du fichier XML n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="70010-132">Editing the XML file directly is not supported.</span></span> <span data-ttu-id="70010-133">Utilisez le composant logiciel enfichable MMC du gestionnaire d’autorisations ou l’API du gestionnaire d’autorisations pour modifier le magasin de stratégies.</span><span class="sxs-lookup"><span data-stu-id="70010-133">Use the Authorization Manager MMC snap-in or the Authorization Manager API to edit the policy store.</span></span>

<span data-ttu-id="70010-134">Le gestionnaire d’autorisations ne prend pas en charge la délégation de l’administration d’un magasin de stratégies XML.</span><span class="sxs-lookup"><span data-stu-id="70010-134">Authorization Manager does not support delegating administration of an XML policy store.</span></span> <span data-ttu-id="70010-135">Pour plus d’informations sur la délégation, consultez délégation [de la définition des autorisations en C++](delegating-the-defining-of-permissions-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="70010-135">For information about delegation, see [Delegating the Defining of Permissions in C++](delegating-the-defining-of-permissions-in-c--.md).</span></span>

<span data-ttu-id="70010-136">L’exemple suivant montre comment créer un objet [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) qui représente un magasin de stratégies d’autorisation dans un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="70010-136">The following example shows how to create an [**AzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object that represents an authorization policy store in an XML file.</span></span>


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



 

 



