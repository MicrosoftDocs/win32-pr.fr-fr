---
description: Crée un conteneur de clé nommé et ajoute une paire de clés de signature et une paire de clés d’échange au conteneur.
ms.assetid: b9d13024-0e53-4930-9962-a2a0d0cb88de
title: 'Exemple de programme C : création d’un conteneur de clé et génération de clés'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e389df22cb4e745cf1c1a65542a17eeabe9b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203990"
---
# <a name="example-c-program-creating-a-key-container-and-generating-keys"></a><span data-ttu-id="ec1aa-103">Exemple de programme C : création d’un conteneur de clé et génération de clés</span><span class="sxs-lookup"><span data-stu-id="ec1aa-103">Example C Program: Creating a Key Container and Generating Keys</span></span>

<span data-ttu-id="ec1aa-104">L’exemple suivant crée un [*conteneur de clé*](../secgloss/k-gly.md) nommé et ajoute une paire de clés de [*signature*](../secgloss/s-gly.md) et une paire de [*clés d’échange*](../secgloss/e-gly.md) au conteneur.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-104">The following example creates a named [*key container*](../secgloss/k-gly.md) and adds a [*signature key pair*](../secgloss/s-gly.md) and an [*exchange key pair*](../secgloss/e-gly.md) to the container.</span></span> <span data-ttu-id="ec1aa-105">Cet exemple peut être exécuté sans problème même si le conteneur de clé nommé et les clés de chiffrement existent déjà.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-105">This example can be run without problem even if the named key container and cryptographic keys already exist.</span></span>

> [!Note]  
> <span data-ttu-id="ec1aa-106">Une application ne doit pas utiliser le conteneur de clé par défaut pour stocker les clés privées.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-106">An application should not use the default key container to store private keys.</span></span> <span data-ttu-id="ec1aa-107">Lorsque plusieurs applications utilisent le même conteneur, une application peut modifier ou détruire les clés dont une autre application a besoin pour être disponible.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-107">When multiple applications use the same container, one application may change or destroy the keys that another application needs to have available.</span></span> <span data-ttu-id="ec1aa-108">Il est recommandé que les applications utilisent des conteneurs de clé liés à l’application.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-108">It is recommended that applications use key containers that are linked to the application.</span></span> <span data-ttu-id="ec1aa-109">Cela réduit le risque que d’autres applications falsifient les clés nécessaires au bon fonctionnement d’une application.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-109">Doing so reduces the risk of other applications tampering with keys that are necessary for an application to function properly.</span></span>

 

<span data-ttu-id="ec1aa-110">Cet exemple illustre les tâches et les fonctions CryptoAPI suivantes :</span><span class="sxs-lookup"><span data-stu-id="ec1aa-110">This example demonstrates the following tasks and CryptoAPI functions:</span></span>

1.  <span data-ttu-id="ec1aa-111">Il tente d’acquérir le conteneur de clé nommé.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-111">It attempts to acquire the named key container.</span></span> <span data-ttu-id="ec1aa-112">Si le conteneur de clé nommé n’existe pas encore, il est créé.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-112">If the named key container does not already exist, it is created.</span></span>
2.  <span data-ttu-id="ec1aa-113">Si une paire de clés de signature n’existe pas dans le conteneur de clé, elle crée une paire de clés de signature dans le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-113">If a signature key pair does not exist in the key container, it creates a signature key pair within the key container.</span></span>
3.  <span data-ttu-id="ec1aa-114">Si une paire de clés d’échange n’existe pas dans le conteneur de clé, elle crée une paire de clés d’échange dans le conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-114">If an exchange key pair does not exist in the key container, it creates an exchange key pair within the key container.</span></span>

<span data-ttu-id="ec1aa-115">Ces opérations ne doivent être exécutées qu’une seule fois pour chaque utilisateur sur chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-115">These operations only need to be performed once for each user on each computer.</span></span> <span data-ttu-id="ec1aa-116">Si le conteneur de clé nommé et les paires de clés ont déjà été créés, cet exemple n’effectue aucune opération.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-116">If the named key container and key pairs have already been created, this sample performs no operations.</span></span>

<span data-ttu-id="ec1aa-117">Cet exemple utilise les fonctions CryptoAPI suivantes :</span><span class="sxs-lookup"><span data-stu-id="ec1aa-117">This example uses the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="ec1aa-118">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="ec1aa-118">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   [<span data-ttu-id="ec1aa-119">**CryptDestroyKey**</span><span class="sxs-lookup"><span data-stu-id="ec1aa-119">**CryptDestroyKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey)
-   [<span data-ttu-id="ec1aa-120">**CryptGenKey**</span><span class="sxs-lookup"><span data-stu-id="ec1aa-120">**CryptGenKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)
-   [<span data-ttu-id="ec1aa-121">**CryptGetUserKey**</span><span class="sxs-lookup"><span data-stu-id="ec1aa-121">**CryptGetUserKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)
-   [<span data-ttu-id="ec1aa-122">**CryptReleaseContext**</span><span class="sxs-lookup"><span data-stu-id="ec1aa-122">**CryptReleaseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

<span data-ttu-id="ec1aa-123">Cet exemple utilise la fonction [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="ec1aa-123">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="ec1aa-124">Le code de cette fonction est inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ec1aa-124">The code for this function is included with the sample.</span></span> <span data-ttu-id="ec1aa-125">Le code pour cette fonction et d’autres fonctions auxiliaires est également listé sous [usage général Functions](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ec1aa-125">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

void main(void) 
{ 
    // Handle for the cryptographic provider context.
    HCRYPTPROV hCryptProv;        
    
    // The name of the container.
    LPCTSTR pszContainerName = TEXT("My Sample Key Container");

    //---------------------------------------------------------------
    // Begin processing. Attempt to acquire a context by using the 
    // specified key container.
    if(CryptAcquireContext(
        &hCryptProv,
        pszContainerName,
        NULL,
        PROV_RSA_FULL,
        0))
    {
        _tprintf(
            TEXT("A crypto context with the %s key container ")
            TEXT("has been acquired.\n"), 
            pszContainerName);
    }
    else
    { 
        //-----------------------------------------------------------
        // Some sort of error occurred in acquiring the context. 
        // This is most likely due to the specified container 
        // not existing. Create a new key container.
        if(GetLastError() == NTE_BAD_KEYSET)
        {
            if(CryptAcquireContext(
                &hCryptProv, 
                pszContainerName, 
                NULL, 
                PROV_RSA_FULL, 
                CRYPT_NEWKEYSET)) 
            {
                _tprintf(TEXT("A new key container has been ")
                    TEXT("created.\n"));
            }
            else
            {
                MyHandleError(TEXT("Could not create a new key ")
                    TEXT("container.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("CryptAcquireContext failed.\n"));
        }
    }

    //---------------------------------------------------------------
    // A context with a key container is available.
    // Attempt to get the handle to the signature key. 

    // Public/private key handle.
    HCRYPTKEY hKey;               
    
    if(CryptGetUserKey(
        hCryptProv,
        AT_SIGNATURE,
        &hKey))
    {
        _tprintf(TEXT("A signature key is available.\n"));
    }
    else
    {
        _tprintf(TEXT("No signature key is available.\n"));
        if(GetLastError() == NTE_NO_KEY) 
        {
            //-------------------------------------------------------
            // The error was that there is a container but no key.

            // Create a signature key pair. 
            _tprintf(TEXT("The signature key does not exist.\n"));
            _tprintf(TEXT("Create a signature key pair.\n")); 
            if(CryptGenKey(
                hCryptProv,
                AT_SIGNATURE,
                0,
                &hKey)) 
            {
                _tprintf(TEXT("Created a signature key pair.\n"));
            }
            else
            {
                MyHandleError(TEXT("Error occurred creating a ")
                    TEXT("signature key.\n")); 
            }
        }
        else
        {
            MyHandleError(TEXT("An error other than NTE_NO_KEY ")
                TEXT("getting a signature key.\n"));
        }
    } // End if.

    _tprintf(TEXT("A signature key pair existed, or one was ")
        TEXT("created.\n\n"));

    // Destroy the signature key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(TEXT("Error during CryptDestroyKey."));
        }

        hKey = NULL;
    } 

    // Next, check the exchange key. 
    if(CryptGetUserKey(
        hCryptProv,
        AT_KEYEXCHANGE,
        &hKey)) 
    {
        _tprintf(TEXT("An exchange key exists.\n"));
    }
    else
    {
        _tprintf(TEXT("No exchange key is available.\n"));

        // Check to determine whether an exchange key 
        // needs to be created.
        if(GetLastError() == NTE_NO_KEY) 
        { 
            // Create a key exchange key pair.
            _tprintf(TEXT("The exchange key does not exist.\n"));
            _tprintf(TEXT("Attempting to create an exchange key ")
                TEXT("pair.\n"));
            if(CryptGenKey(
                hCryptProv,
                AT_KEYEXCHANGE,
                0,
                &hKey)) 
            {
                _tprintf(TEXT("Exchange key pair created.\n"));
            }
            else
            {
                MyHandleError(TEXT("Error occurred attempting to ")
                    TEXT("create an exchange key.\n"));
            }
        }
        else
        {
            MyHandleError(TEXT("An error other than NTE_NO_KEY ")
                TEXT("occurred.\n"));
        }
    }

    // Destroy the exchange key.
    if(hKey)
    {
        if(!(CryptDestroyKey(hKey)))
        {
            MyHandleError(TEXT("Error during CryptDestroyKey."));
        }

        hKey = NULL;
    }

    // Release the CSP.
    if(hCryptProv)
    {
        if(!(CryptReleaseContext(hCryptProv, 0)))
        {
            MyHandleError(TEXT("Error during CryptReleaseContext."));
        }
    } 
    
    _tprintf(TEXT("Everything is okay. A signature key "));
    _tprintf(TEXT("pair and an exchange key exist in "));
    _tprintf(TEXT("the %s key container.\n"), pszContainerName);  
} // End main.
```



 

 
