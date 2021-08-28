---
description: 'Cryptography API : Next Generation (CNG) fournit des fonctions qui interrogent, ajoutent, suppriment et hiérarchisent les suites de chiffrement prises en charge par un fournisseur. Les modifications apportées à l’aide de ces fonctions prennent effet immédiatement et ne nécessitent pas le redémarrage d’un serveur actif.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Hiérarchisation des suites de chiffrement Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4436d2f72ebaa1f8d551d935ea9f16d2c03cd7c75fc7d40a73f1a27c7406ad6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920768"
---
# <a name="prioritizing-schannel-cipher-suites"></a>Hiérarchisation des suites de chiffrement Schannel

[CRYPTOGRAPHY API : Next Generation](../seccng/cng-portal.md) (CNG) fournit des fonctions qui interrogent, ajoutent, suppriment et hiérarchisent les suites de chiffrement prises en charge par un fournisseur. Les modifications apportées à l’aide de ces fonctions prennent effet immédiatement et ne nécessitent pas le redémarrage d’un serveur actif.

> [!Note]
> Vous pouvez également modifier la liste des suites de chiffrement en configurant les paramètres de stratégie de groupe ordre de la **suite de chiffrement SSL** à l’aide du composant logiciel enfichable objet stratégie de groupe de la console MMC (Microsoft Management Console).
> 
> **Pour configurer le paramètre de stratégie de groupe ordre de la **suite de chiffrement SSL****
> 
> 1.  À l’invite de commandes, entrez **gpedit. msc**. L' **éditeur d’objets de stratégie de groupe** s’affiche.
> 2.  développez **configuration ordinateur**, **Modèles d’administration**, **réseau**, puis cliquez sur **Paramètres de configuration SSL**.
> 3.  sous **Configuration ssl Paramètres**, cliquez sur le paramètre ordre de la **Suite de chiffrement ssl** .
> 4.  Dans le volet ordre de la **suite de chiffrement SSL** , faites défiler le volet vers le bas.
> 5.  Suivez les instructions indiquées **dans la rubrique Comment modifier ce paramètre**.
> 
> Il est nécessaire de redémarrer l’ordinateur après avoir modifié ce paramètre pour que les modifications prennent effet.

 

La liste de suites de chiffrement est limitée à 1023 caractères.

Pour hiérarchiser les suites de chiffrement Schannel, consultez les exemples suivants.

-   [Liste des suites de chiffrement prises en charge](#listing-supported-cipher-suites)
-   [Ajout, suppression et hiérarchisation des suites de chiffrement](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a>Liste des suites de chiffrement prises en charge

Appelez la fonction [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) pour répertorier les suites de chiffrement prises en charge par un fournisseur par ordre de priorité.

L’exemple suivant montre comment utiliser la fonction [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) pour répertorier les suites de chiffrement prises en charge.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{

   HRESULT Status = ERROR_SUCCESS;
   DWORD   cbBuffer = 0;
   PCRYPT_CONTEXT_FUNCTIONS pBuffer = NULL;

    Status = BCryptEnumContextFunctions(
        CRYPT_LOCAL,
        L"SSL",
        NCRYPT_SCHANNEL_INTERFACE,
        &cbBuffer,
        &pBuffer);
    if(FAILED(Status))
    {
        printf_s("\n**** Error 0x%x returned by BCryptEnumContextFunctions\n", Status);
        goto Cleanup;
    }
                
    if(pBuffer == NULL)
    {
        printf_s("\n**** Error pBuffer returned from BCryptEnumContextFunctions is null");
        goto Cleanup;
    }

    printf_s("\n\n Listing Cipher Suites ");
    for(UINT index = 0; index < pBuffer->cFunctions; ++index)
    {
        printf_s("\n%S", pBuffer->rgpszFunctions[index]);
    }

Cleanup:
    if (pBuffer != NULL)
    {
        BCryptFreeBuffer(pBuffer);
    }
}


```



## <a name="adding-removing-and-prioritizing-cipher-suites"></a>Ajout, suppression et hiérarchisation des suites de chiffrement

Appelez les fonctions [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) et [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) pour ajouter et supprimer des suites de chiffrement dans la liste des suites de chiffrement prises en charge.

Lorsque vous ajoutez une suite de chiffrement, définissez la valeur du paramètre *dwPosition* de la fonction [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) sur **énigmatique \_ Priority \_ Top** pour l’ajouter au début de la liste hiérarchisée, ou pour **crypter la \_ priorité en \_ bas** pour l’ajouter au bas de la liste.

Pour classer par ordre de priorité la liste des suites de chiffrement, supprimez toutes les suites de chiffrement de la liste, puis ajoutez des suites de chiffrement à la liste dans l’ordre de votre choix.

L’exemple suivant montre comment ajouter une suite de chiffrement en haut de la liste classée par priorité pour le fournisseur Microsoft Schannel par défaut.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
    LPWSTR wszCipher = (L"RSA_EXPORT1024_DES_CBC_SHA");
       
    Status = BCryptAddContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher,
                CRYPT_PRIORITY_TOP);
}


```



L’exemple suivant montre comment supprimer une suite de chiffrement de la liste classée par ordre de priorité pour le fournisseur Microsoft Schannel par défaut.


```C++
#include <stdio.h>
#include <windows.h>
#include <bcrypt.h>


void main()
{
    
    SECURITY_STATUS Status = ERROR_SUCCESS;
      LPWSTR wszCipher = (L"TLS_RSA_WITH_RC4_128_SHA");
       
    Status = BCryptRemoveContextFunction(
                CRYPT_LOCAL,
                L"SSL",
                NCRYPT_SCHANNEL_INTERFACE,
                wszCipher);
}


```



 

 
