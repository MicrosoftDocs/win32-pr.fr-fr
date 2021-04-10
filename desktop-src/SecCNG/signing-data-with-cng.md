---
description: La signature des données ne protège pas les données. Elle vérifie uniquement l’intégrité des données.
ms.assetid: 8f0ace5a-c8f9-4a45-8500-041a9f22637d
title: Signature de données avec CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 658dd1c9a833cfb15b708a7f85013e3d9cacac9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115175"
---
# <a name="signing-data-with-cng"></a><span data-ttu-id="8ddbd-104">Signature de données avec CNG</span><span class="sxs-lookup"><span data-stu-id="8ddbd-104">Signing Data with CNG</span></span>

<span data-ttu-id="8ddbd-105">La signature des données ne protège pas les données.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-105">Data signing does not protect the data.</span></span> <span data-ttu-id="8ddbd-106">Elle vérifie uniquement l’intégrité des données.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-106">It only to verifies the integrity of the data.</span></span> <span data-ttu-id="8ddbd-107">L’expéditeur hache ces données et signe (chiffre) le hachage à l’aide d’une clé privée.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-107">The sender hashes that data and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="8ddbd-108">Le destinataire prévu effectue la vérification en créant un hachage des données reçues, en déchiffrant la signature pour obtenir le hachage d’origine et en comparant les deux hachages.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-108">The intended recipient performs verification by creating a hash of the data received, decrypting the signature to obtain the original hash, and comparing the two hashes.</span></span>

<span data-ttu-id="8ddbd-109">Lorsque les données sont signées, l’expéditeur crée une valeur de [*hachage*](/windows/desktop/SecGloss/h-gly) et signe (chiffre) le hachage à l’aide d’une clé privée.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-109">When data is signed, the sender creates a [*hash*](/windows/desktop/SecGloss/h-gly) value and signs (encrypts) the hash by using a private key.</span></span> <span data-ttu-id="8ddbd-110">Cette signature est ensuite attachée aux données et envoyée dans un message à un destinataire.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-110">This signature is then attached to the data and sent in a message to a recipient.</span></span> <span data-ttu-id="8ddbd-111">L’algorithme de hachage utilisé pour créer la signature doit être connu à l’avance par le destinataire ou identifié dans le message.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-111">The hashing algorithm that was used to create the signature must be known in advance by the recipient or identified in the message.</span></span> <span data-ttu-id="8ddbd-112">Cette opération est effectuée dans le protocole de message.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-112">How this is done is up to the message protocol.</span></span>

<span data-ttu-id="8ddbd-113">Pour vérifier la signature, le destinataire extrait les données et la signature du message.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-113">To verify the signature, the recipient extracts the data and the signature from the message.</span></span> <span data-ttu-id="8ddbd-114">Le destinataire crée ensuite une autre valeur de hachage à partir des données, déchiffre le hachage signé à l’aide de la clé publique de l’expéditeur et compare les deux valeurs de hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-114">The recipient then creates another hash value from the data, decrypts the signed hash by using the sender's public key, and compares the two hash values.</span></span> <span data-ttu-id="8ddbd-115">Si les valeurs sont identiques, la signature a été vérifiée et les données sont supposées être inchangées.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-115">If the values are identical, the signature has been verified and the data is assumed to be unaltered.</span></span>

<span data-ttu-id="8ddbd-116">**Pour créer une signature à l’aide de CNG**</span><span class="sxs-lookup"><span data-stu-id="8ddbd-116">**To create a signature by using CNG**</span></span>

1.  <span data-ttu-id="8ddbd-117">Créez une valeur de hachage pour les données à l’aide des fonctions de hachage CNG.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-117">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="8ddbd-118">Pour plus d’informations sur la création d’un hachage, consultez [création d’un hachage avec CNG](creating-a-hash-with-cng.md).</span><span class="sxs-lookup"><span data-stu-id="8ddbd-118">For more information about creating a hash, see [Creating a Hash With CNG](creating-a-hash-with-cng.md).</span></span>
2.  <span data-ttu-id="8ddbd-119">Créez une clé asymétrique pour signer le hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-119">Create an asymmetric key to sign the hash.</span></span> <span data-ttu-id="8ddbd-120">Vous pouvez créer une clé persistante avec les [fonctions de stockage de clé CNG](cng-key-storage-functions.md) ou une clé éphémère avec les fonctions de la [primitive de chiffrement CNG](cng-cryptographic-primitive-functions.md).</span><span class="sxs-lookup"><span data-stu-id="8ddbd-120">You can either create a persistent key with the [CNG Key Storage Functions](cng-key-storage-functions.md) or an ephemeral key with the [CNG Cryptographic Primitive Functions](cng-cryptographic-primitive-functions.md).</span></span>
3.  <span data-ttu-id="8ddbd-121">Utilisez la fonction [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) ou [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) pour signer (chiffrer) la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-121">Use either the [**NCryptSignHash**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsignhash) or the [**BCryptSignHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsignhash) function to sign (encrypt) the hash value.</span></span> <span data-ttu-id="8ddbd-122">Cette fonction signe la valeur de hachage à l’aide de la clé asymétrique.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-122">This function signs the hash value by using the asymmetric key.</span></span>
4.  <span data-ttu-id="8ddbd-123">Combiner les données et la signature dans un message qui peut être envoyé au destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-123">Combine the data and signature into a message which can be sent sent to the intended recipient.</span></span>

<span data-ttu-id="8ddbd-124">**Pour vérifier une signature à l’aide de CNG**</span><span class="sxs-lookup"><span data-stu-id="8ddbd-124">**To verify a signature by using CNG**</span></span>

1.  <span data-ttu-id="8ddbd-125">Extrayez les données et la signature du message.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-125">Extract the data and signature from the message.</span></span>
2.  <span data-ttu-id="8ddbd-126">Créez une valeur de hachage pour les données à l’aide des fonctions de hachage CNG.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-126">Create a hash value for the data by using the CNG hashing functions.</span></span> <span data-ttu-id="8ddbd-127">L’algorithme de hachage utilisé doit être le même que celui utilisé pour signer le hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-127">The hashing algorithm used must be the same algorithm that was used to sign he hash.</span></span>
3.  <span data-ttu-id="8ddbd-128">Obtenez la partie publique de la paire de clés asymétriques qui a été utilisée pour signer le hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-128">Obtain the public portion of the asymmetric key pair that was used to sign the hash.</span></span> <span data-ttu-id="8ddbd-129">La façon dont vous obtenez cette clé dépend de la façon dont la clé a été créée et rendue persistante.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-129">How you obtain this key depends on how the key was created and persisted.</span></span> <span data-ttu-id="8ddbd-130">Si la clé a été créée ou chargée avec les [fonctions de stockage de clé CNG](cng-key-storage-functions.md), vous allez utiliser la fonction [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) pour charger la clé persistante.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-130">If the key was created or loaded with the [CNG Key Storage Functions](cng-key-storage-functions.md), you will use the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function to load the persisted key.</span></span> <span data-ttu-id="8ddbd-131">Si la clé est une clé éphémère, elle devrait avoir été enregistrée dans un objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-131">If the key is an ephemeral key, then it would have to have been saved to a key BLOB.</span></span> <span data-ttu-id="8ddbd-132">Vous devez passer cet objet BLOB de clé à la fonction [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) ou [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="8ddbd-132">You need to pass this key BLOB to either the [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) or the [**NCryptImportKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptimportkey) function.</span></span>
4.  <span data-ttu-id="8ddbd-133">Transmettez la nouvelle valeur de hachage, la signature et le handle de clé à la fonction [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) ou [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) .</span><span class="sxs-lookup"><span data-stu-id="8ddbd-133">Pass the new hash value, the signature, and the key handle to either the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) or the [**BCryptVerifySignature**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptverifysignature) function.</span></span> <span data-ttu-id="8ddbd-134">Ces fonctions effectuent la vérification à l’aide de la clé publique pour déchiffrer la signature et en comparant le hachage déchiffré au hachage calculé à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-134">These functions perform verification by using the public key to decrypt the signature and comparing the decrypted hash to the hash computed in step 2.</span></span> <span data-ttu-id="8ddbd-135">La fonction **BCryptVerifySignature** retourne l' **état \_ Success** si la signature correspond à la signature de hachage ou d' **état \_ \_ non valide** si la signature ne correspond pas au hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-135">The **BCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **STATUS\_INVALID\_SIGNATURE** if the signature does not match the hash.</span></span> <span data-ttu-id="8ddbd-136">La fonction **NCryptVerifySignature** retourne l' **état \_ Success** si la signature correspond à la **\_ \_ signature incorrecte** Hash ou NPD si la signature ne correspond pas au hachage.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-136">The **NCryptVerifySignature** function will return **STATUS\_SUCCESS** if the signature matches the hash or **NTE\_BAD\_SIGNATURE** if the signature does not match the hash.</span></span>

## <a name="signing-and-verifying-data-example"></a><span data-ttu-id="8ddbd-137">Exemple de signature et de vérification des données</span><span class="sxs-lookup"><span data-stu-id="8ddbd-137">Signing and Verifying Data Example</span></span>

<span data-ttu-id="8ddbd-138">L’exemple suivant montre comment utiliser les API de chiffrement primitif pour signer des données avec une clé persistante et vérifier la signature avec une clé éphémère.</span><span class="sxs-lookup"><span data-stu-id="8ddbd-138">The following example shows how to use the cryptographic primitive APIs to sign data with a persisted key and verify the signature with an ephemeral key.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for ECDSA 256 signing using CNG
    
    Example for use of BCrypt/NCrypt API
    
    Persisted key for signing and ephemeral key for verification

--*/

#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>
#include <ncrypt.h>


#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const  BYTE rgbMsg[] =
{
    0x04, 0x87, 0xec, 0x66, 0xa8, 0xbf, 0x17, 0xa6,
    0xe3, 0x62, 0x6f, 0x1a, 0x55, 0xe2, 0xaf, 0x5e,
    0xbc, 0x54, 0xa4, 0xdc, 0x68, 0x19, 0x3e, 0x94,
};

void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{
    NCRYPT_PROV_HANDLE      hProv           = NULL;
    NCRYPT_KEY_HANDLE       hKey            = NULL;
    BCRYPT_KEY_HANDLE       hTmpKey         = NULL;
    SECURITY_STATUS         secStatus       = ERROR_SUCCESS;
    BCRYPT_ALG_HANDLE       hHashAlg        = NULL,
                            hSignAlg        = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbBlob          = 0,
                            cbSignature     = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL,
                            pbBlob          = NULL,
                            pbSignature     = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hHashAlg,
                                                BCRYPT_SHA1_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hSignAlg,
                                                BCRYPT_ECDSA_P256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_OBJECT_LENGTH, 
                                        (PBYTE)&cbHashObject, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash object on the heap
    pbHashObject = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHashObject);
    if(NULL == pbHashObject)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

   //calculate the length of the hash
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hHashAlg, 
                                        BCRYPT_HASH_LENGTH, 
                                        (PBYTE)&cbHash, 
                                        sizeof(DWORD), 
                                        &cbData, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptGetProperty\n", status);
        goto Cleanup;
    }

    //allocate the hash buffer on the heap
    pbHash = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbHash);
    if(NULL == pbHash)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    //create a hash
    if(!NT_SUCCESS(status = BCryptCreateHash(
                                        hHashAlg, 
                                        &hHash, 
                                        pbHashObject, 
                                        cbHashObject, 
                                        NULL, 
                                        0, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptCreateHash\n", status);
        goto Cleanup;
    }
    

    //hash some data
    if(!NT_SUCCESS(status = BCryptHashData(
                                        hHash,
                                        (PBYTE)rgbMsg,
                                        sizeof(rgbMsg),
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptHashData\n", status);
        goto Cleanup;
    }
    
    //close the hash
    if(!NT_SUCCESS(status = BCryptFinishHash(
                                        hHash, 
                                        pbHash, 
                                        cbHash, 
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptFinishHash\n", status);
        goto Cleanup;
    }

    //open handle to KSP
    if(FAILED(secStatus = NCryptOpenStorageProvider(
                                                &hProv, 
                                                MS_KEY_STORAGE_PROVIDER, 
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptOpenStorageProvider\n", secStatus);
        goto Cleanup;
    }

    //create a persisted key
    if(FAILED(secStatus = NCryptCreatePersistedKey(
                                                hProv,
                                                &hKey,
                                                NCRYPT_ECDSA_P256_ALGORITHM,
                                                L"my ecc key",
                                                0,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptCreatePersistedKey\n", secStatus);
        goto Cleanup;
    }

    //create key on disk
    if(FAILED(secStatus = NCryptFinalizeKey(hKey, 0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptFinalizeKey\n", secStatus);
        goto Cleanup;
    }

    //sign the hash
    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    NULL,
                                    0,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }


    //allocate the signature buffer
    pbSignature = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbSignature);
    if(NULL == pbSignature)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptSignHash(
                                    hKey,
                                    NULL,
                                    pbHash,
                                    cbHash,
                                    pbSignature,
                                    cbSignature,
                                    &cbSignature,
                                    0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptSignHash\n", secStatus);
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        NULL,
                                        0,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    pbBlob = (PBYTE)HeapAlloc (GetProcessHeap (), 0, cbBlob);
    if(NULL == pbBlob)
    {
        wprintf(L"**** memory allocation failed\n");
        goto Cleanup;
    }

    if(FAILED(secStatus = NCryptExportKey(
                                        hKey,
                                        NULL,
                                        BCRYPT_ECCPUBLIC_BLOB,
                                        NULL,
                                        pbBlob,
                                        cbBlob,
                                        &cbBlob,
                                        0)))
    {
        wprintf(L"**** Error 0x%x returned by NCryptExportKey\n", secStatus);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptImportKeyPair(
                                            hSignAlg,
                                            NULL,
                                            BCRYPT_ECCPUBLIC_BLOB,
                                            &hTmpKey,
                                            pbBlob,
                                            cbBlob,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptImportKeyPair\n", status);
        goto Cleanup;
    }

    if(!NT_SUCCESS(status = BCryptVerifySignature(
                                            hTmpKey,
                                            NULL,
                                            pbHash,
                                            cbHash,
                                            pbSignature,
                                            cbSignature,
                                            0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptVerifySignature\n", status);
        goto Cleanup;
    }

    wprintf(L"Success!\n");

Cleanup:

    if(hHashAlg)
    {
        BCryptCloseAlgorithmProvider(hHashAlg,0);
    }

    if(hSignAlg)
    {
        BCryptCloseAlgorithmProvider(hSignAlg,0);
    }

    if (hHash)    
    {
        BCryptDestroyHash(hHash);
    }

    if(pbHashObject)
    {
        HeapFree(GetProcessHeap(), 0, pbHashObject);
    }

    if(pbHash)
    {
        HeapFree(GetProcessHeap(), 0, pbHash);
    }

    if(pbSignature)
    {
        HeapFree(GetProcessHeap(), 0, pbSignature);
    }

    if(pbBlob)
    {
        HeapFree(GetProcessHeap(), 0, pbBlob);
    }

    if (hTmpKey)    
    {
        BCryptDestroyKey(hTmpKey);
    }

    if (hKey)    
    {
        NCryptDeleteKey(hKey, 0);
    }

    if (hProv)    
    {
        NCryptFreeObject(hProv);
    }    
}


```



 

 
