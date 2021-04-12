---
description: 'Cryptography API : Next Generation (CNG) fournit des fonctions qui interrogent, ajoutent, suppriment et hiérarchisent les suites de chiffrement prises en charge par un fournisseur. Les modifications apportées à l’aide de ces fonctions prennent effet immédiatement et ne nécessitent pas le redémarrage d’un serveur actif.'
ms.assetid: e919be5c-ac2c-446c-a422-971805b1f672
title: Hiérarchisation des suites de chiffrement Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f885c4d51006233be252a02c7cc3bebd26a4e6c3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104211319"
---
# <a name="prioritizing-schannel-cipher-suites"></a><span data-ttu-id="16993-104">Hiérarchisation des suites de chiffrement Schannel</span><span class="sxs-lookup"><span data-stu-id="16993-104">Prioritizing Schannel Cipher Suites</span></span>

<span data-ttu-id="16993-105">[CRYPTOGRAPHY API : Next Generation](../seccng/cng-portal.md) (CNG) fournit des fonctions qui interrogent, ajoutent, suppriment et hiérarchisent les suites de chiffrement prises en charge par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="16993-105">[Cryptography API: Next Generation](../seccng/cng-portal.md) (CNG) provides functions that query, add, remove, and prioritize the cipher suites that a provider supports.</span></span> <span data-ttu-id="16993-106">Les modifications apportées à l’aide de ces fonctions prennent effet immédiatement et ne nécessitent pas le redémarrage d’un serveur actif.</span><span class="sxs-lookup"><span data-stu-id="16993-106">Changes made by using these functions take effect immediately and do not require restarting an active server.</span></span>

> [!Note]
> <span data-ttu-id="16993-107">Vous pouvez également modifier la liste des suites de chiffrement en configurant les paramètres de stratégie de groupe ordre de la **suite de chiffrement SSL** à l’aide du composant logiciel enfichable objet stratégie de groupe de la console MMC (Microsoft Management Console).</span><span class="sxs-lookup"><span data-stu-id="16993-107">You can also modify the list of cipher suites by configuring the **SSL Cipher Suite Order** group policy settings using the Group Policy Object snap-in in Microsoft Management Console.</span></span>
> 
> <span data-ttu-id="16993-108">\*\*Pour configurer le paramètre de stratégie de groupe ordre de la \*\*suite de chiffrement SSL\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="16993-108">**To configure the **SSL Cipher Suite Order** group policy setting**</span></span>
> 
> 1.  <span data-ttu-id="16993-109">À l’invite de commandes, entrez **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="16993-109">At a command prompt, enter **gpedit.msc**.</span></span> <span data-ttu-id="16993-110">L' **éditeur d’objets de stratégie de groupe** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="16993-110">The **Group Policy Object Editor** appears.</span></span>
> 2.  <span data-ttu-id="16993-111">Développez **Configuration ordinateur**, **modèles d’administration**, **réseau**, puis cliquez sur **paramètres de configuration SSL**.</span><span class="sxs-lookup"><span data-stu-id="16993-111">Expand **Computer Configuration**, **Administrative Templates**, **Network**, and then click **SSL Configuration Settings**.</span></span>
> 3.  <span data-ttu-id="16993-112">Sous **paramètres de configuration SSL**, cliquez sur le paramètre ordre de la **suite de chiffrement SSL** .</span><span class="sxs-lookup"><span data-stu-id="16993-112">Under **SSL Configuration Settings**, click the **SSL Cipher Suite Order** setting.</span></span>
> 4.  <span data-ttu-id="16993-113">Dans le volet ordre de la **suite de chiffrement SSL** , faites défiler le volet vers le bas.</span><span class="sxs-lookup"><span data-stu-id="16993-113">In the **SSL Cipher Suite Order** pane, scroll to the bottom of the pane.</span></span>
> 5.  <span data-ttu-id="16993-114">Suivez les instructions indiquées **dans la rubrique Comment modifier ce paramètre**.</span><span class="sxs-lookup"><span data-stu-id="16993-114">Follow the instructions labeled **How to modify this setting**.</span></span>
> 
> <span data-ttu-id="16993-115">Il est nécessaire de redémarrer l’ordinateur après avoir modifié ce paramètre pour que les modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="16993-115">It is necessary to restart the computer after modifying this setting for the changes to take effect.</span></span>

 

<span data-ttu-id="16993-116">La liste de suites de chiffrement est limitée à 1023 caractères.</span><span class="sxs-lookup"><span data-stu-id="16993-116">The list of cipher suites is limited to 1023 characters.</span></span>

<span data-ttu-id="16993-117">Pour hiérarchiser les suites de chiffrement Schannel, consultez les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="16993-117">To prioritize Schannel cipher suites, see the following examples.</span></span>

-   [<span data-ttu-id="16993-118">Liste des suites de chiffrement prises en charge</span><span class="sxs-lookup"><span data-stu-id="16993-118">Listing Supported Cipher Suites</span></span>](#listing-supported-cipher-suites)
-   [<span data-ttu-id="16993-119">Ajout, suppression et hiérarchisation des suites de chiffrement</span><span class="sxs-lookup"><span data-stu-id="16993-119">Adding, Removing, and Prioritizing Cipher Suites</span></span>](#adding-removing-and-prioritizing-cipher-suites)

## <a name="listing-supported-cipher-suites"></a><span data-ttu-id="16993-120">Liste des suites de chiffrement prises en charge</span><span class="sxs-lookup"><span data-stu-id="16993-120">Listing Supported Cipher Suites</span></span>

<span data-ttu-id="16993-121">Appelez la fonction [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) pour répertorier les suites de chiffrement prises en charge par un fournisseur par ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="16993-121">Call the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list the cipher suites that a provider supports in order of priority.</span></span>

<span data-ttu-id="16993-122">L’exemple suivant montre comment utiliser la fonction [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) pour répertorier les suites de chiffrement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="16993-122">The following example demonstrates how to use the [**BCryptEnumContextFunctions**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptenumcontextfunctions) function to list supported cipher suites.</span></span>


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



## <a name="adding-removing-and-prioritizing-cipher-suites"></a><span data-ttu-id="16993-123">Ajout, suppression et hiérarchisation des suites de chiffrement</span><span class="sxs-lookup"><span data-stu-id="16993-123">Adding, Removing, and Prioritizing Cipher Suites</span></span>

<span data-ttu-id="16993-124">Appelez les fonctions [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) et [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) pour ajouter et supprimer des suites de chiffrement dans la liste des suites de chiffrement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="16993-124">Call the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) and [**BCryptRemoveContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptremovecontextfunction) functions to add and remove cipher suites from the list of supported cipher suites.</span></span>

<span data-ttu-id="16993-125">Lorsque vous ajoutez une suite de chiffrement, définissez la valeur du paramètre *dwPosition* de la fonction [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) sur **énigmatique \_ Priority \_ Top** pour l’ajouter au début de la liste hiérarchisée, ou pour **crypter la \_ priorité en \_ bas** pour l’ajouter au bas de la liste.</span><span class="sxs-lookup"><span data-stu-id="16993-125">When adding a cipher suite, set the value of the *dwPosition* parameter of the [**BCryptAddContextFunction**](/windows/win32/api/bcrypt/nf-bcrypt-bcryptaddcontextfunction) function to **CRYPT\_PRIORITY\_TOP** to add it to the top of the prioritized list, or to **CRYPT\_PRIORITY\_BOTTOM** to add it to the bottom of the list.</span></span>

<span data-ttu-id="16993-126">Pour classer par ordre de priorité la liste des suites de chiffrement, supprimez toutes les suites de chiffrement de la liste, puis ajoutez des suites de chiffrement à la liste dans l’ordre de votre choix.</span><span class="sxs-lookup"><span data-stu-id="16993-126">To prioritize the list of cipher suites, remove all of the cipher suites from the list, and then add cipher suites to the list in the order you want them.</span></span>

<span data-ttu-id="16993-127">L’exemple suivant montre comment ajouter une suite de chiffrement en haut de la liste classée par priorité pour le fournisseur Microsoft Schannel par défaut.</span><span class="sxs-lookup"><span data-stu-id="16993-127">The following example shows how to add a cipher suite to the top of the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



<span data-ttu-id="16993-128">L’exemple suivant montre comment supprimer une suite de chiffrement de la liste classée par ordre de priorité pour le fournisseur Microsoft Schannel par défaut.</span><span class="sxs-lookup"><span data-stu-id="16993-128">The following example shows how to remove a cipher suite from the prioritized list for the default Microsoft Schannel Provider.</span></span>


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



 

 
