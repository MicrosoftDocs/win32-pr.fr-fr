---
description: L’exemple suivant crée et duplique un hachage d’un texte. Il ajoute ensuite du texte supplémentaire au hachage d’origine et à un autre texte dans le doublon.
ms.assetid: 7aa7c9a1-471b-4b40-9967-b1da946c83a5
title: 'Exemple de programme C : duplication d’un hachage'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a418f1e5e615d8c4b4c0e8a0af3061b9b6f860e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530838"
---
# <a name="example-c-program-duplicating-a-hash"></a><span data-ttu-id="afdba-104">Exemple de programme C : duplication d’un hachage</span><span class="sxs-lookup"><span data-stu-id="afdba-104">Example C Program: Duplicating a Hash</span></span>

<span data-ttu-id="afdba-105">L’exemple suivant crée et duplique un [*hachage*](../secgloss/h-gly.md) d’un texte.</span><span class="sxs-lookup"><span data-stu-id="afdba-105">The following example creates and duplicates a [*hash*](../secgloss/h-gly.md) of some text.</span></span> <span data-ttu-id="afdba-106">Il ajoute ensuite du texte supplémentaire au hachage d’origine et à un autre texte dans le doublon.</span><span class="sxs-lookup"><span data-stu-id="afdba-106">It then adds additional text to the original hash and different text to the duplicate.</span></span>

<span data-ttu-id="afdba-107">Cet exemple utilise les fonctions CryptoAPI suivantes :</span><span class="sxs-lookup"><span data-stu-id="afdba-107">This example uses the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="afdba-108">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="afdba-108">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
-   [<span data-ttu-id="afdba-109">**CryptCreateHash**</span><span class="sxs-lookup"><span data-stu-id="afdba-109">**CryptCreateHash**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
-   [<span data-ttu-id="afdba-110">**CryptHashData**</span><span class="sxs-lookup"><span data-stu-id="afdba-110">**CryptHashData**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)
-   [<span data-ttu-id="afdba-111">**CryptDuplicateHash**</span><span class="sxs-lookup"><span data-stu-id="afdba-111">**CryptDuplicateHash**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash)
-   [<span data-ttu-id="afdba-112">**CryptGetHashParam**</span><span class="sxs-lookup"><span data-stu-id="afdba-112">**CryptGetHashParam**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam)
-   [<span data-ttu-id="afdba-113">**CryptDestroyHash**</span><span class="sxs-lookup"><span data-stu-id="afdba-113">**CryptDestroyHash**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash)
-   [<span data-ttu-id="afdba-114">**CryptReleaseContext**</span><span class="sxs-lookup"><span data-stu-id="afdba-114">**CryptReleaseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext)

<span data-ttu-id="afdba-115">Cet exemple utilise la fonction [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="afdba-115">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="afdba-116">Le code pour cette fonction est inclus à la fin de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="afdba-116">Code for this function is included at the end of the example.</span></span> <span data-ttu-id="afdba-117">Le code pour cette fonction et d’autres fonctions auxiliaires est également listé sous [usage général Functions](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="afdba-117">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);
void Get_And_Print_Hash(HCRYPTHASH hHash);

void main(void)
{
    //--------------------------------------------------------------------
    // Copyright (C) Microsoft.  All rights reserved.
    // Declare and initialize variables.
    HCRYPTPROV   hCryptProv = NULL;
    HCRYPTHASH   hOriginalHash;
    HCRYPTHASH   hDuplicateHash;

    //--------------------------------------------------------------------
    // Acquire a cryptographic provider context handle.
    if(CryptAcquireContext(
       &hCryptProv,
       NULL,
       NULL,
       PROV_RSA_FULL,
       0))
    {
        printf("CryptAcquireContext succeeded. \n");
    }
    else
    {
        MyHandleError("Error during CryptAcquireContext!");
    }

    //--------------------------------------------------------------------
    // Create a hash.
    if (CryptCreateHash(
        hCryptProv,
        CALG_SHA1,
        0,
        0,
        &hOriginalHash))
    {
       printf("An empty hash object has been created. \n");
    }
    else
    {
       MyHandleError("Error during CryptCreateHash.");
    }

    //--------------------------------------------------------------------
    // Hash a BYTE string.
    if (CryptHashData(
        hOriginalHash,
        (BYTE*)"Some Common Data",
        sizeof("Some Common Data"), 0))
    {
       printf("An original hash has been created. \n");
    }
    else
    {
       MyHandleError("Error during CryptHashData.");
    }

    //--------------------------------------------------------------------
    // Duplicate the hash.
    if (CryptDuplicateHash(
       hOriginalHash,
       NULL,
       0,
       &hDuplicateHash))
    {
       printf("The hash has been duplicated. \n");
    }
    else
    {
       MyHandleError("Error during CryptDuplicateHash.");
    }

    printf("The original hash -- phase 1.\n");
    Get_And_Print_Hash(hOriginalHash);

    printf("The duplicate hash -- phase 1.\n");
    Get_And_Print_Hash(hDuplicateHash);

    //--------------------------------------------------------------------
    // Hash some data with the original hash.
    if (CryptHashData(
         hOriginalHash,
         (BYTE*)"Some Data",
         sizeof("Some Data"),
         0))
    {
        printf("Additional data has been hashed with the original. \n");
    }
    else
    {
        MyHandleError("Error during CryptHashData.");
    }

    //--------------------------------------------------------------------
    // Hash other data with the duplicate hash.
    if (CryptHashData(
         hDuplicateHash,
         (BYTE*)"Other Data",
         sizeof("Other Data"),
         0))
    {
       printf("More data has been hashed with the duplicate. \n");
    }
    else
    {
       MyHandleError("Error during CryptHashData.");
    }

    printf("The original hash -- phase 2.\n");
    Get_And_Print_Hash(hOriginalHash);

    printf("The duplicate hash -- phase 2.\n");
    Get_And_Print_Hash(hDuplicateHash);

    // Destroy the original hash.
    if(CryptDestroyHash(hOriginalHash))
    {
       printf("The original hash has been destroyed. \n");
    }
    else
    {
       MyHandleError("ERROR during CryptDestroyHash");
    }

    //--------------------------------------------------------------------
    // Destroy the duplicate hash.
    if (CryptDestroyHash(hDuplicateHash))
    {
       printf("The duplicate hash has been destroyed. \n");
    }
    else
    {
       MyHandleError("Error -- CryptDestroyHash");
    }

    //--------------------------------------------------------------------
    // Release the CSP.

    if(hCryptProv)
       CryptReleaseContext(hCryptProv,0);

    printf("The program ran to completion without error. \n");
} // end main

//--------------------------------------------------------------------
// Define the function Get_And_Print_Hash.
void Get_And_Print_Hash(HCRYPTHASH hOHash)
{
    //--------------------------------------------------------------------
    // Declare and initialize local variables.
    HCRYPTHASH   hHash;
    BYTE         *pbHash;
    DWORD        dwHashLen;
    DWORD        dwHashLenSize = sizeof(DWORD);
    DWORD        i;

    //--------------------------------------------------------------------
    // Duplicate the hash passed in.
    // The hash is duplicated to leave the original hash intact.

    if (CryptDuplicateHash(
       hOHash,
       NULL,
       0,
       &hHash))
    {
        // It worked. Do nothing.
    }
    else
    {
       MyHandleError("Error during CryptDuplicateHash.");
    }

    if(CryptGetHashParam(
       hHash,
       HP_HASHSIZE,
       (BYTE *)&dwHashLen,
       &dwHashLenSize,
       0))
    {
        // It worked. Do nothing.
    }
    else
    {
        MyHandleError("CryptGetHashParam failed to get size.");
    }

    if(pbHash = (BYTE*)malloc(dwHashLen))
    {
        // It worked. Do nothing.
    }
    else
    {
         MyHandleError("Allocation failed.");
    }

    if(CryptGetHashParam(
       hHash,
       HP_HASHVAL,
       pbHash,
       &dwHashLen,
       0))
    {
        // Print the hash value.
        printf("The hash is:  ");
        for(i = 0 ; i < dwHashLen ; i++)
        {
           printf("%02x ",pbHash[i]);
        }
        printf("\n");
    }
    else
    {
        MyHandleError("Error during reading hash value.");
    }

    free(pbHash);
    if (CryptDestroyHash(hHash))
    {
        // It worked. Do nothing.
    }
    else
    {
       MyHandleError("ERROR - CryptDestroyHash");
    }
} // end Get_And_Print_Hash


//--------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit
// the program.
// For most applications, replace this function with one
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
