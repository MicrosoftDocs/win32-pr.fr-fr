---
description: L’exemple suivant crée une clé de session aléatoire, duplique la clé, définit des paramètres supplémentaires sur la clé d’origine et détruit à la fois l’original et les clés dupliquées.
ms.assetid: e57274cf-42d3-445b-97f1-dd574010290f
title: 'Exemple de programme C : duplication d’une clé de session'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38934d399a6a38f14e551e79d4e1f877dbadf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951878"
---
# <a name="example-c-program-duplicating-a-session-key"></a><span data-ttu-id="da198-103">Exemple de programme C : duplication d’une clé de session</span><span class="sxs-lookup"><span data-stu-id="da198-103">Example C Program: Duplicating a Session Key</span></span>

<span data-ttu-id="da198-104">L’exemple suivant crée une [*clé de session*](../secgloss/s-gly.md)aléatoire, duplique la clé, définit des paramètres supplémentaires sur la clé d’origine et détruit à la fois l’original et les clés dupliquées.</span><span class="sxs-lookup"><span data-stu-id="da198-104">The following example creates a random [*session key*](../secgloss/s-gly.md), duplicates the key, sets some additional parameters on the original key, and destroys both the original and the duplicate keys.</span></span> <span data-ttu-id="da198-105">Cet exemple illustre l’utilisation de [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) et des fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="da198-105">This example illustrates the use of [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey) and related functions.</span></span>

<span data-ttu-id="da198-106">Cet exemple illustre les tâches et les fonctions CryptoAPI suivantes :</span><span class="sxs-lookup"><span data-stu-id="da198-106">This example illustrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="da198-107">Accès à un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) à l’aide de [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="da198-107">Accessing a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="da198-108">Création d’une clé de session à l’aide de [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span><span class="sxs-lookup"><span data-stu-id="da198-108">Creating a session key using [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).</span></span>
-   <span data-ttu-id="da198-109">Duplication de la clé créée à l’aide de [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey).</span><span class="sxs-lookup"><span data-stu-id="da198-109">Duplicating the key created using [**CryptDuplicateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey).</span></span>
-   <span data-ttu-id="da198-110">L’utilisation de [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) pour modifier le processus de génération de clé de deux manières différentes.</span><span class="sxs-lookup"><span data-stu-id="da198-110">Using [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) to alter the key generation process in two different ways.</span></span>
-   <span data-ttu-id="da198-111">Remplissage d’une mémoire tampon avec des octets aléatoires à l’aide de [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span><span class="sxs-lookup"><span data-stu-id="da198-111">Filling a buffer with random bytes using [**CryptGenRandom**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom).</span></span>
-   <span data-ttu-id="da198-112">Destruction des clés à l’aide de [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="da198-112">Destroying the keys using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span>
-   <span data-ttu-id="da198-113">Libération du CSP avec [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span><span class="sxs-lookup"><span data-stu-id="da198-113">Releasing the CSP with [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>

<span data-ttu-id="da198-114">Cet exemple utilise la fonction [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="da198-114">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="da198-115">Le code de cette fonction est inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="da198-115">The code for this function is included with the sample.</span></span> <span data-ttu-id="da198-116">Le code pour cette fonction et d’autres fonctions auxiliaires est également listé sous [usage général Functions](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="da198-116">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Begin main.

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV   hCryptProv;
HCRYPTKEY    hOriginalKey;
HCRYPTKEY    hDuplicateKey;
DWORD        dwMode;
BYTE         pbData[16];

//-------------------------------------------------------------------
// Begin processing.

printf("This program creates a session key and duplicates \n");
printf("that key. Next, parameters are added to the original \n");
printf("key. Finally, both keys are destroyed. \n\n");

//-------------------------------------------------------------------
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
    MyHandleError("Error during CryptAcquireContext!\n");
}
//-------------------------------------------------------------------
// Generate a key.
if (CryptGenKey(
     hCryptProv, 
     CALG_RC4, 
     0, 
     &hOriginalKey))
{
   printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR - CryptGenKey.");
}
//-------------------------------------------------------------------
// Duplicate the key.

if (CryptDuplicateKey(
     hOriginalKey, 
     NULL, 
     0, 
     &hDuplicateKey))
{
   printf("The session key has been duplicated. \n");
}
else
{
   MyHandleError("ERROR - CryptDuplicateKey");
}
//-------------------------------------------------------------------
// Set additional parameters on the original key.
// First, set the cipher mode.

dwMode = CRYPT_MODE_ECB;
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_MODE, 
   (BYTE*)&dwMode, 
   0)) 
{
     printf("Key Parameters set. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
// Generate a random initialization vector.
if(CryptGenRandom(
   hCryptProv, 
   8, 
   pbData)) 
{
     printf("Random sequence generated. \n");
}
else
{
     MyHandleError("Error during CryptGenRandom.");
}
//-------------------------------------------------------------------
// Set the initialization vector.
if(CryptSetKeyParam(
   hOriginalKey, 
   KP_IV, 
   pbData, 
   0)) 
{
     printf("Parameter set with random sequence as "
         "initialization vector. \n");
}
else
{
     MyHandleError("Error during CryptSetKeyParam.");
}
//-------------------------------------------------------------------
// Clean up.

if (hOriginalKey)
    if (!CryptDestroyKey(hOriginalKey))
        MyHandleError("Failed CryptDestroyKey\n");

if (hDuplicateKey)
    if (!CryptDestroyKey(hDuplicateKey))
            MyHandleError("Failed CryptDestroyKey\n");

if(hCryptProv)
    if (!CryptReleaseContext(hCryptProv, 0))
        MyHandleError("Failed CryptReleaseContext\n");

printf("\nThe program ran to completion without error. \n");

} // End of main.

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 
