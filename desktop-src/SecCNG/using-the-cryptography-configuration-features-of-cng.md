---
description: Fournit des fonctions pour énumérer et obtenir des informations sur les fournisseurs inscrits.
ms.assetid: 5b07060e-0c66-4bf2-b697-05231cb38375
title: Utilisation des fonctionnalités de configuration de la cryptographie CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd700b52810f43381722a315bec12216acd7b683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515252"
---
# <a name="using-the-cryptography-configuration-features-of-cng"></a><span data-ttu-id="0452f-103">Utilisation des fonctionnalités de configuration de la cryptographie CNG</span><span class="sxs-lookup"><span data-stu-id="0452f-103">Using the Cryptography Configuration Features of CNG</span></span>

<span data-ttu-id="0452f-104">L’API CNG fournit des fonctions pour énumérer et obtenir des informations sur les fournisseurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="0452f-104">The CNG API provides functions to enumerate and obtain information about registered providers.</span></span>

-   [<span data-ttu-id="0452f-105">Énumération des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="0452f-105">Enumerating Providers</span></span>](#enumerating-providers)
-   [<span data-ttu-id="0452f-106">Obtention des informations d’inscription du fournisseur</span><span class="sxs-lookup"><span data-stu-id="0452f-106">Getting Provider Registration Information</span></span>](#getting-provider-registration-information)

## <a name="enumerating-providers"></a><span data-ttu-id="0452f-107">Énumération des fournisseurs</span><span class="sxs-lookup"><span data-stu-id="0452f-107">Enumerating Providers</span></span>

<span data-ttu-id="0452f-108">Vous utilisez la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) pour énumérer les fournisseurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="0452f-108">You use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to enumerate the registered providers.</span></span> <span data-ttu-id="0452f-109">La fonction **BCryptEnumRegisteredProviders** peut être appelée de deux manières :</span><span class="sxs-lookup"><span data-stu-id="0452f-109">The **BCryptEnumRegisteredProviders** function can be called in one of two ways:</span></span>

1.  <span data-ttu-id="0452f-110">La première consiste à faire en sorte que la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) alloue la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0452f-110">The first is to have the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function allocate the memory.</span></span> <span data-ttu-id="0452f-111">Pour ce faire, vous devez transmettre l’adresse d’un pointeur **null** pour le paramètre *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="0452f-111">This is accomplished by passing the address of a **NULL** pointer for the *ppBuffer* parameter.</span></span> <span data-ttu-id="0452f-112">Ce code alloue la mémoire requise pour la structure des [**\_ fournisseurs**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) de chiffrement et les chaînes associées.</span><span class="sxs-lookup"><span data-stu-id="0452f-112">This code will allocate the memory required for the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and the associated strings.</span></span> <span data-ttu-id="0452f-113">Lorsque la fonction **BCryptEnumRegisteredProviders** est utilisée de cette manière, vous devez libérer la mémoire lorsqu’elle n’est plus nécessaire en passant *ppBuffer* à la fonction [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .</span><span class="sxs-lookup"><span data-stu-id="0452f-113">When the **BCryptEnumRegisteredProviders** function is used in this manner, you must free the memory when it is no longer needed by passing *ppBuffer* to the [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) function.</span></span>

    <span data-ttu-id="0452f-114">L’exemple suivant montre comment utiliser la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) pour allouer la mémoire tampon pour vous.</span><span class="sxs-lookup"><span data-stu-id="0452f-114">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate the buffer for you.</span></span>

    ```C++
    #include <windows.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders1()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;
        PCRYPT_PROVIDERS pBuffer = NULL;

        /*
        Get the providers, letting the BCryptEnumRegisteredProviders 
        function allocate the memory.
        */
        status = BCryptEnumRegisteredProviders(&cbBuffer, &pBuffer);

        if (NT_SUCCESS(status))
        {
            if (pBuffer != NULL)
            {
                // Enumerate the providers.
                for (ULONG i = 0; i < pBuffer->cProviders; i++)
                {
                    printf("%S\n", pBuffer->rgpszProviders[i]);
                }
            }
        }
        else
        {
            printf("BCryptEnumRegisteredProviders failed with error " 
                "code 0x%08x\n", status);
        }

        if (NULL != pBuffer)
        {
            /*
            Free the memory allocated by the 
            BCryptEnumRegisteredProviders function.
            */
            BCryptFreeBuffer(pBuffer);
        }
    }
    
    ```

    

2.  <span data-ttu-id="0452f-115">La deuxième méthode consiste à allouer vous-même la mémoire requise.</span><span class="sxs-lookup"><span data-stu-id="0452f-115">The second method is to allocate the required memory yourself.</span></span> <span data-ttu-id="0452f-116">Pour ce faire, vous devez appeler la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) avec la **valeur null** pour le paramètre *ppBuffer* .</span><span class="sxs-lookup"><span data-stu-id="0452f-116">This is accomplished by calling the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function with **NULL** for the *ppBuffer* parameter.</span></span> <span data-ttu-id="0452f-117">La fonction **BCryptEnumRegisteredProviders** sera placée dans la valeur vers laquelle pointe le paramètre *pcbBuffer* , la taille requise, en octets, de la structure des [**\_ fournisseurs**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) de chiffre et de toutes les chaînes.</span><span class="sxs-lookup"><span data-stu-id="0452f-117">The **BCryptEnumRegisteredProviders** function will place in the value pointed to by the *pcbBuffer* parameter, the required size, in bytes, of the [**CRYPT\_PROVIDERS**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) structure and all strings.</span></span> <span data-ttu-id="0452f-118">Vous allouez ensuite la mémoire requise et vous transmettez l’adresse de ce pointeur de mémoire tampon pour le paramètre *ppBuffer* dans un deuxième appel à la fonction **BCryptEnumRegisteredProviders** .</span><span class="sxs-lookup"><span data-stu-id="0452f-118">You then allocate the required memory and pass the address of this buffer pointer for the *ppBuffer* parameter in a second call to the **BCryptEnumRegisteredProviders** function.</span></span>

    <span data-ttu-id="0452f-119">L’exemple suivant montre comment utiliser la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) pour allouer et utiliser votre propre mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0452f-119">The following example shows how to use the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function to allocate and use your own buffer.</span></span>

    ```C++
    #include <windows.h>
    #include <stdio.h>

    #ifndef NT_SUCCESS
    #define NT_SUCCESS(Status) ((NTSTATUS)(Status) >= 0)
    #endif

    void EnumProviders2()
    {
        NTSTATUS status;
        ULONG cbBuffer = 0;

        // Get the required size of the buffer.
        status = BCryptEnumRegisteredProviders(&cbBuffer, NULL);

        if (STATUS_BUFFER_TOO_SMALL == status)
        {
            // Allocate the buffer.
            PCRYPT_PROVIDERS pBuffer = 
                (PCRYPT_PROVIDERS)LocalAlloc(LPTR, cbBuffer);
            if (NULL != pBuffer)
            {
                // Get the providers in the buffer that was allocated.
                status = BCryptEnumRegisteredProviders(
                    &cbBuffer, 
                    &pBuffer);
                if (NT_SUCCESS(status))
                {
                    for (ULONG i = 0; i < pBuffer->cProviders; i++)
                    {
                        // Enumerate the providers.
                        printf("%S\n", pBuffer->rgpszProviders[i]);
                    }
                }

                // Free the memory that was allocated.
                LocalFree(pBuffer);
            }
        }
    }
    
    ```

    

## <a name="getting-provider-registration-information"></a><span data-ttu-id="0452f-120">Obtention des informations d’inscription du fournisseur</span><span class="sxs-lookup"><span data-stu-id="0452f-120">Getting Provider Registration Information</span></span>

<span data-ttu-id="0452f-121">La fonction [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) est utilisée pour obtenir des informations supplémentaires spécifiques à l’inscription sur un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0452f-121">The [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function is used to obtain additional, registration-specific information about a provider.</span></span> <span data-ttu-id="0452f-122">Cette fonction prend le nom du fournisseur pour lequel vous souhaitez obtenir des informations, le mode du fournisseur souhaité (mode noyau, mode utilisateur, ou les deux) et l’identificateur de l’interface du fournisseur pour lequel récupérer les informations d’inscription.</span><span class="sxs-lookup"><span data-stu-id="0452f-122">This function takes the name of the provider that you want to obtain information for, the desired provider mode (kernel mode, user mode, or both), and the identifier of the provider interface to retrieve the registration information for.</span></span> <span data-ttu-id="0452f-123">Par exemple, pour obtenir les informations d’inscription du mode utilisateur pour l’interface de chiffrement pour le fournisseur « fournisseur primitif Microsoft », vous devez effectuer un appel similaire à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="0452f-123">For example, to obtain the user mode registration information for the cipher interface for the "Microsoft Primitive Provider" provider, you would make a call similar to the following.</span></span>


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



<span data-ttu-id="0452f-124">À l’instar de la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , la fonction [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) peut soit allouer de la mémoire pour vous, soit vous pouvez allouer la mémoire vous-même.</span><span class="sxs-lookup"><span data-stu-id="0452f-124">Like the [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) function, the [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) function can either allocate memory for you or you can allocate the memory yourself.</span></span> <span data-ttu-id="0452f-125">Le processus est le même pour les deux fonctions.</span><span class="sxs-lookup"><span data-stu-id="0452f-125">The process is the same for the two functions.</span></span>

 

 



