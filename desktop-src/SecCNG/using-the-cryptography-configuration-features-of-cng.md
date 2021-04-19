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
# <a name="using-the-cryptography-configuration-features-of-cng"></a>Utilisation des fonctionnalités de configuration de la cryptographie CNG

L’API CNG fournit des fonctions pour énumérer et obtenir des informations sur les fournisseurs inscrits.

-   [Énumération des fournisseurs](#enumerating-providers)
-   [Obtention des informations d’inscription du fournisseur](#getting-provider-registration-information)

## <a name="enumerating-providers"></a>Énumération des fournisseurs

Vous utilisez la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) pour énumérer les fournisseurs inscrits. La fonction **BCryptEnumRegisteredProviders** peut être appelée de deux manières :

1.  La première consiste à faire en sorte que la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) alloue la mémoire. Pour ce faire, vous devez transmettre l’adresse d’un pointeur **null** pour le paramètre *ppBuffer* . Ce code alloue la mémoire requise pour la structure des [**\_ fournisseurs**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) de chiffrement et les chaînes associées. Lorsque la fonction **BCryptEnumRegisteredProviders** est utilisée de cette manière, vous devez libérer la mémoire lorsqu’elle n’est plus nécessaire en passant *ppBuffer* à la fonction [**BCryptFreeBuffer**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfreebuffer) .

    L’exemple suivant montre comment utiliser la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) pour allouer la mémoire tampon pour vous.

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

    

2.  La deuxième méthode consiste à allouer vous-même la mémoire requise. Pour ce faire, vous devez appeler la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) avec la **valeur null** pour le paramètre *ppBuffer* . La fonction **BCryptEnumRegisteredProviders** sera placée dans la valeur vers laquelle pointe le paramètre *pcbBuffer* , la taille requise, en octets, de la structure des [**\_ fournisseurs**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_providers) de chiffre et de toutes les chaînes. Vous allouez ensuite la mémoire requise et vous transmettez l’adresse de ce pointeur de mémoire tampon pour le paramètre *ppBuffer* dans un deuxième appel à la fonction **BCryptEnumRegisteredProviders** .

    L’exemple suivant montre comment utiliser la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) pour allouer et utiliser votre propre mémoire tampon.

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

    

## <a name="getting-provider-registration-information"></a>Obtention des informations d’inscription du fournisseur

La fonction [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) est utilisée pour obtenir des informations supplémentaires spécifiques à l’inscription sur un fournisseur. Cette fonction prend le nom du fournisseur pour lequel vous souhaitez obtenir des informations, le mode du fournisseur souhaité (mode noyau, mode utilisateur, ou les deux) et l’identificateur de l’interface du fournisseur pour lequel récupérer les informations d’inscription. Par exemple, pour obtenir les informations d’inscription du mode utilisateur pour l’interface de chiffrement pour le fournisseur « fournisseur primitif Microsoft », vous devez effectuer un appel similaire à ce qui suit.


```C++
BCryptQueryProviderRegistration(
    MS_PRIMITIVE_PROVIDER,
    CRYPT_UM,
    BCRYPT_CIPHER_INTERFACE,
    //...
    );

```



À l’instar de la fonction [**BCryptEnumRegisteredProviders**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptenumregisteredproviders) , la fonction [**BCryptQueryProviderRegistration**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptqueryproviderregistration) peut soit allouer de la mémoire pour vous, soit vous pouvez allouer la mémoire vous-même. Le processus est le même pour les deux fonctions.

 

 



