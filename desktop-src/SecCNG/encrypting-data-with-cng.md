---
description: CNG vous permet de chiffrer les données à l’aide d’un nombre minimal d’appels de fonction et vous permet d’effectuer toute la gestion de la mémoire.
ms.assetid: 40622282-e190-40d0-80d4-cab9eddc2091
title: Chiffrement des données avec CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f161cd23ec6863bee7f5ffd5b696fa99880e3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514771"
---
# <a name="encrypting-data-with-cng"></a><span data-ttu-id="3e28d-103">Chiffrement des données avec CNG</span><span class="sxs-lookup"><span data-stu-id="3e28d-103">Encrypting Data with CNG</span></span>

<span data-ttu-id="3e28d-104">L’utilisation principale d’une API de chiffrement consiste à chiffrer et à déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="3e28d-104">The primary use of any cryptography API is to encrypt and decrypt data.</span></span> <span data-ttu-id="3e28d-105">CNG vous permet de chiffrer les données à l’aide d’un nombre minimal d’appels de fonction et vous permet d’effectuer toute la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3e28d-105">CNG allows you to encrypt data by using a minimum number of function calls and allows you to perform all of the memory management.</span></span> <span data-ttu-id="3e28d-106">Alors que la plupart des détails de l’implémentation du protocole sont laissés à l’utilisateur, CNG fournit les primitives qui effectuent les tâches réelles de chiffrement et de déchiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="3e28d-106">While many of the protocol implementation details are left up to the user, CNG provides the primitives that perform the actual data encryption and decryption tasks.</span></span>

-   [<span data-ttu-id="3e28d-107">Chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="3e28d-107">Encrypting Data</span></span>](#encrypting-data-with-cng)
-   [<span data-ttu-id="3e28d-108">Exemple de chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="3e28d-108">Encrypting Data Example</span></span>](#encrypting-data-example)
-   [<span data-ttu-id="3e28d-109">Déchiffrement de données</span><span class="sxs-lookup"><span data-stu-id="3e28d-109">Decrypting Data</span></span>](#decrypting-data)

## <a name="encrypting-data"></a><span data-ttu-id="3e28d-110">Chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="3e28d-110">Encrypting Data</span></span>

<span data-ttu-id="3e28d-111">Pour chiffrer les données, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3e28d-111">To encrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="3e28d-112">Ouvrez un fournisseur d’algorithme qui prend en charge le chiffrement, tel que **BCRYPT \_ des \_ algorithmes**.</span><span class="sxs-lookup"><span data-stu-id="3e28d-112">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="3e28d-113">Créez une clé avec laquelle chiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="3e28d-113">Create a key to encrypt the data with.</span></span> <span data-ttu-id="3e28d-114">Une clé peut être créée à l’aide de l’une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e28d-114">A key can be created by using any of the following functions:</span></span>
    -   <span data-ttu-id="3e28d-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) ou [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) pour les fournisseurs asymétriques.</span><span class="sxs-lookup"><span data-stu-id="3e28d-115">[**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) or [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) for asymmetric providers.</span></span>
    -   <span data-ttu-id="3e28d-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) ou [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) pour les fournisseurs symétriques.</span><span class="sxs-lookup"><span data-stu-id="3e28d-116">[**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) or [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) for symmetric providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="3e28d-117">Le chiffrement et le déchiffrement des données avec une clé asymétrique sont gourmands en calculs par rapport au chiffrement à clé symétrique.</span><span class="sxs-lookup"><span data-stu-id="3e28d-117">Data encryption and decryption with an asymmetric key is computationally intensive compared to symmetric key encryption.</span></span> <span data-ttu-id="3e28d-118">Si vous devez chiffrer les données avec une clé asymétrique, vous devez chiffrer les données avec une clé symétrique, chiffrer la clé symétrique avec une clé asymétrique et inclure la clé symétrique chiffrée avec le message.</span><span class="sxs-lookup"><span data-stu-id="3e28d-118">If you need to encrypt data with an asymmetric key, you should encrypt the data with a symmetric key, encrypt the symmetric key with an asymmetric key, and include the encrypted symmetric key with the message.</span></span> <span data-ttu-id="3e28d-119">Le destinataire peut ensuite déchiffrer la clé symétrique et utiliser la clé symétrique pour déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="3e28d-119">The recipient can then decrypt the symmetric key and use the symmetric key to decrypt the data.</span></span>

     

3.  <span data-ttu-id="3e28d-120">Obtenir la taille des données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="3e28d-120">Obtain the size of the encrypted data.</span></span> <span data-ttu-id="3e28d-121">Cela est basé sur l’algorithme de chiffrement, le schéma de remplissage (le cas échéant) et la taille des données à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="3e28d-121">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be encrypted.</span></span> <span data-ttu-id="3e28d-122">Vous pouvez obtenir la taille des données chiffrées à l’aide de la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) , en transmettant la **valeur null** pour le paramètre *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3e28d-122">You can obtain the encrypted data size by using the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="3e28d-123">Tous les autres paramètres doivent être les mêmes que lorsque les données sont réellement chiffrées, à l’exception du paramètre *pbInput* , qui n’est pas utilisé dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="3e28d-123">All other parameters must be the same as when the data is actually encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="3e28d-124">Vous pouvez chiffrer les données sur place avec la même mémoire tampon ou chiffrer les données dans une mémoire tampon distincte.</span><span class="sxs-lookup"><span data-stu-id="3e28d-124">You can either encrypt the data in place with the same buffer or encrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="3e28d-125">Si vous souhaitez chiffrer les données en place, transmettez le pointeur de mémoire tampon en texte clair pour les paramètres *pbInput* et *pbOutput* dans la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="3e28d-125">If you want to encrypt the data in place, pass the plaintext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function.</span></span> <span data-ttu-id="3e28d-126">Il est possible que la taille des données chiffrées soit supérieure à la taille des données non chiffrées, de sorte que la mémoire tampon de texte en clair doit être suffisamment grande pour contenir les données chiffrées, pas seulement le texte en clair.</span><span class="sxs-lookup"><span data-stu-id="3e28d-126">It is possible that the encrypted data size will be larger than the unencrypted data size, so the plaintext buffer must be large enough to hold the encrypted data, not just the plaintext.</span></span> <span data-ttu-id="3e28d-127">Vous pouvez utiliser la taille obtenue à l’étape 3 pour allouer la mémoire tampon de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="3e28d-127">You can use the size obtained in step 3 to allocate the plaintext buffer.</span></span>

    <span data-ttu-id="3e28d-128">Si vous souhaitez chiffrer les données dans une mémoire tampon distincte, allouez une mémoire tampon pour les données chiffrées à l’aide de la taille obtenue à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="3e28d-128">If you want to encrypt the data into a separate buffer, allocate a memory buffer for the encrypted data by using the size obtained in step 3.</span></span>

5.  <span data-ttu-id="3e28d-129">Appelez la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) pour chiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="3e28d-129">Call the [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) function to encrypt the data.</span></span> <span data-ttu-id="3e28d-130">Cette fonction écrira les données chiffrées à l’emplacement fourni dans le paramètre *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3e28d-130">This function will write the encrypted data to the location provided in the *pbOutput* parameter.</span></span>
6.  <span data-ttu-id="3e28d-131">Rendez les données chiffrées persistantes si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3e28d-131">Persist the encrypted data as needed.</span></span>
7.  <span data-ttu-id="3e28d-132">Répétez les étapes 5 et 6 jusqu’à ce que toutes les données aient été chiffrées.</span><span class="sxs-lookup"><span data-stu-id="3e28d-132">Repeat steps 5 and 6 until all of the data has been encrypted.</span></span>

## <a name="encrypting-data-example"></a><span data-ttu-id="3e28d-133">Exemple de chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="3e28d-133">Encrypting Data Example</span></span>

<span data-ttu-id="3e28d-134">L’exemple suivant montre comment chiffrer des données avec CNG à l’aide de l’algorithme de chiffrement symétrique Advanced Encryption Standard.</span><span class="sxs-lookup"><span data-stu-id="3e28d-134">The following example shows how to encrypt data with CNG by using the advanced encryption standard symmetric encryption algorithm.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:
    Sample program for AES-CBC encryption using CNG

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>

#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


#define DATA_TO_ENCRYPT  "Test Data"


const BYTE rgbPlaintext[] = 
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbIV[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07,
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

static const BYTE rgbAES128Key[] =
{
    0x00, 0x01, 0x02, 0x03, 0x04, 0x05, 0x06, 0x07, 
    0x08, 0x09, 0x0A, 0x0B, 0x0C, 0x0D, 0x0E, 0x0F
};

void PrintBytes(
                IN BYTE     *pbPrintData,
                IN DWORD    cbDataLen)
{
    DWORD dwCount = 0;

    for(dwCount=0; dwCount < cbDataLen;dwCount++)
    {
        printf("0x%02x, ",pbPrintData[dwCount]);

        if(0 == (dwCount + 1 )%10) putchar('\n');
    }

}

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAesAlg                     = NULL;
    BCRYPT_KEY_HANDLE       hKey                        = NULL;
    NTSTATUS                status                      = STATUS_UNSUCCESSFUL;
    DWORD                   cbCipherText                = 0, 
                            cbPlainText                 = 0,
                            cbData                      = 0, 
                            cbKeyObject                 = 0,
                            cbBlockLen                  = 0,
                            cbBlob                      = 0;
    PBYTE                   pbCipherText                = NULL,
                            pbPlainText                 = NULL,
                            pbKeyObject                 = NULL,
                            pbIV                        = NULL,
                            pbBlob                      = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);


    // Open an algorithm handle.
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAesAlg,
                                                BCRYPT_AES_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    // Calculate the size of the buffer to hold the KeyObject.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbKeyObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Allocate the key object on the heap.
    pbKeyObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbKeyObject);
    if(NULL == pbKeyObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   // Calculate the block length for the IV.
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAesAlg, 
                                        BCRYPT_BLOCK_LENGTH, 
                                        (PBYTE)&cbBlockLen, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    // Determine whether the cbBlockLen is not longer than the IV length.
    if (cbBlockLen > sizeof (rgbIV))
    {
        wprintf (L"**** block length is longer than the provided IV length\n");
        goto Cleanup;
    }

    // Allocate a buffer for the IV. The buffer is consumed during the 
    // encrypt/decrypt process.
    pbIV= (PBYTE) HeapAlloc (GetProcessHeap (), 0, cbBlockLen);
    if(NULL == pbIV)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbIV, rgbIV, cbBlockLen);

    if(!NT_SUCCESS(status = BCryptSetProperty(
                                hAesAlg, 
                                BCRYPT_CHAINING_MODE, 
                                (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
                                sizeof(BCRYPT_CHAIN_MODE_CBC), 
                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptSetProperty\n", status);
        goto Cleanup;
    }

                

     // Generate the key from supplied input key bytes.
    if(!NT_SUCCESS(status = BCryptGenerateSymmetricKey(
                                        hAesAlg, 
                                        &hKey, 
                                        pbKeyObject, 
                                        cbKeyObject, 
                                        (PBYTE)rgbAES128Key, 
                                        sizeof(rgbAES128Key), 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }

  
    // Save another copy of the key for later.
    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }


    // Allocate the buffer to hold the BLOB.
    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptExportKey(
                                        hKey, 
                                        NULL, 
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        pbBlob, 
                                        cbBlob, 
                                        &cbBlob, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptExportKey\n", status);
        goto Cleanup;
    }
 
    cbPlainText = sizeof(rgbPlaintext);
    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    memcpy(pbPlainText, rgbPlaintext, sizeof(rgbPlaintext));
    
    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen,
                                        NULL, 
                                        0, 
                                        &cbCipherText, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    pbCipherText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbCipherText);
    if(NULL == pbCipherText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    // Use the key to encrypt the plaintext buffer.
    // For block sized messages, block padding will add an extra block.
    if(!NT_SUCCESS(status = BCryptEncrypt(
                                        hKey, 
                                        pbPlainText, 
                                        cbPlainText,
                                        NULL,
                                        pbIV,
                                        cbBlockLen, 
                                        pbCipherText, 
                                        cbCipherText, 
                                        &cbData, 
                                        BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptEncrypt\n", status);
        goto Cleanup;
    }

    // Destroy the key and reimport from saved BLOB.
    if(!NT_SUCCESS(status = BCryptDestroyKey(hKey)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDestroyKey\n", status);
        goto Cleanup;
    }    
    hKey = 0;

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    pbPlainText = NULL;

    // We can reuse the key object.
    memset(pbKeyObject, 0 , cbKeyObject);

    
    // Reinitialize the IV because encryption would have modified it.
    memcpy(pbIV, rgbIV, cbBlockLen);


    if(!NT_SUCCESS(status = BCryptImportKey(
                                        hAesAlg,
                                        NULL,
                                        BCRYPT_OPAQUE_KEY_BLOB,
                                        &hKey,
                                        pbKeyObject,
                                        cbKeyObject,
                                        pbBlob,
                                        cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGenerateSymmetricKey\n", status);
        goto Cleanup;
    }
       

    //
    // Get the output buffer size.
    //
    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV,
                                    cbBlockLen,
                                    NULL, 
                                    0, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }

    pbPlainText = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbPlainText);
    if(NULL == pbPlainText)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptDecrypt(
                                    hKey, 
                                    pbCipherText, 
                                    cbCipherText, 
                                    NULL,
                                    pbIV, 
                                    cbBlockLen,
                                    pbPlainText, 
                                    cbPlainText, 
                                    &cbPlainText, 
                                    BCRYPT_BLOCK_PADDING)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptDecrypt\n", status);
        goto Cleanup;
    }


    if (0 != memcmp(pbPlainText, (PBYTE)rgbPlaintext, sizeof(rgbPlaintext))) 
    {
        wprintf(L"Expected decrypted text comparison failed.\n");
        goto Cleanup;
    } 

    wprintf(L"Success!\n");


Cleanup:

    if(hAesAlg)
    {
        BCryptCloseAlgorithmProvider(hAesAlg,0);
    }

    if (hKey)    
    {
        BCryptDestroyKey(hKey);
    }

    if(pbCipherText)
    {
        HeapFree(GetProcessHeap(), 0, pbCipherText);
    }

    if(pbPlainText)
    {
        HeapFree(GetProcessHeap(), 0, pbPlainText);
    }

    if(pbKeyObject)
    {
        HeapFree(GetProcessHeap(), 0, pbKeyObject);
    }

    if(pbIV)
    {
        HeapFree(GetProcessHeap(), 0, pbIV);
    }

}
```



## <a name="decrypting-data"></a><span data-ttu-id="3e28d-135">Déchiffrement de données</span><span class="sxs-lookup"><span data-stu-id="3e28d-135">Decrypting Data</span></span>

<span data-ttu-id="3e28d-136">Pour déchiffrer des données, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3e28d-136">To decrypt data, perform the following steps:</span></span>

1.  <span data-ttu-id="3e28d-137">Ouvrez un fournisseur d’algorithme qui prend en charge le chiffrement, tel que **BCRYPT \_ des \_ algorithmes**.</span><span class="sxs-lookup"><span data-stu-id="3e28d-137">Open an algorithm provider that supports encryption, such as **BCRYPT\_DES\_ALGORITHM**.</span></span>
2.  <span data-ttu-id="3e28d-138">Obtenez la clé avec laquelle les données ont été chiffrées et utilisez cette clé pour obtenir un handle pour la clé.</span><span class="sxs-lookup"><span data-stu-id="3e28d-138">Obtain the key that the data was encrypted with, and use that key to obtain a handle for the key.</span></span>
3.  <span data-ttu-id="3e28d-139">Obtenir la taille des données déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="3e28d-139">Obtain the size of the decrypted data.</span></span> <span data-ttu-id="3e28d-140">Cela est basé sur l’algorithme de chiffrement, le schéma de remplissage (le cas échéant) et la taille des données à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="3e28d-140">This is based on the encryption algorithm, the padding scheme (if any), and the size of the data to be decrypted.</span></span> <span data-ttu-id="3e28d-141">Vous pouvez obtenir la taille des données chiffrées à l’aide de la fonction [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , en transmettant la **valeur null** pour le paramètre *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3e28d-141">You can obtain the encrypted data size by using the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function, passing **NULL** for the *pbOutput* parameter.</span></span> <span data-ttu-id="3e28d-142">Les paramètres qui spécifient le schéma de remplissage et le [*vecteur d’initialisation*](/windows/desktop/SecGloss/i-gly) (IV) doivent être les mêmes que lorsque les données ont été chiffrées, à l’exception du paramètre *pbInput* , qui n’est pas utilisé dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="3e28d-142">The parameters that specify the padding scheme and [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) must be the same as when the data was encrypted except for the *pbInput* parameter, which is not used in this case.</span></span>
4.  <span data-ttu-id="3e28d-143">Allouez une mémoire tampon pour les données déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="3e28d-143">Allocate a memory buffer for the decrypted data.</span></span>
5.  <span data-ttu-id="3e28d-144">Vous pouvez déchiffrer les données en place à l’aide de la même mémoire tampon, ou déchiffrer les données dans une mémoire tampon distincte.</span><span class="sxs-lookup"><span data-stu-id="3e28d-144">You can either decrypt the data in place by using the same buffer, or decrypt the data into a separate buffer.</span></span>

    <span data-ttu-id="3e28d-145">Si vous souhaitez déchiffrer les données sur place, transmettez le pointeur de mémoire tampon de texte chiffré pour les paramètres *pbInput* et *pbOutput* dans la fonction [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="3e28d-145">If you want to decrypt the data in place, pass the ciphertext buffer pointer for both the *pbInput* and *pbOutput* parameters in the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function.</span></span>

    <span data-ttu-id="3e28d-146">Si vous souhaitez déchiffrer les données dans une mémoire tampon distincte, allouez une mémoire tampon pour les données déchiffrées à l’aide de la taille obtenue à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="3e28d-146">If you want to decrypt the data into a separate buffer, allocate a memory buffer for the decrypted data by using the size obtained in step 3.</span></span>

6.  <span data-ttu-id="3e28d-147">Appelez la fonction [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) pour déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="3e28d-147">Call the [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) function to decrypt the data.</span></span> <span data-ttu-id="3e28d-148">Les paramètres qui spécifient le modèle de remplissage et le vecteur d’alimentation doivent être les mêmes que lorsque les données ont été chiffrées.</span><span class="sxs-lookup"><span data-stu-id="3e28d-148">The parameters that specify the padding scheme and IV must be the same as when the data was encrypted.</span></span> <span data-ttu-id="3e28d-149">Cette fonction écrira les données déchiffrées à l’emplacement fourni dans le paramètre *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3e28d-149">This function will write the decrypted data to the location provided in the *pbOutput* parameter.</span></span>
7.  <span data-ttu-id="3e28d-150">Rendez les données déchiffrées persistantes si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3e28d-150">Persist the decrypted data as needed.</span></span>
8.  <span data-ttu-id="3e28d-151">Répétez les étapes 5 et 6 jusqu’à ce que toutes les données soient déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="3e28d-151">Repeat steps 5 and 6 until all of the data has been decrypted.</span></span>

 

 
