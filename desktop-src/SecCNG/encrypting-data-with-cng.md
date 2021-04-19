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
# <a name="encrypting-data-with-cng"></a>Chiffrement des données avec CNG

L’utilisation principale d’une API de chiffrement consiste à chiffrer et à déchiffrer les données. CNG vous permet de chiffrer les données à l’aide d’un nombre minimal d’appels de fonction et vous permet d’effectuer toute la gestion de la mémoire. Alors que la plupart des détails de l’implémentation du protocole sont laissés à l’utilisateur, CNG fournit les primitives qui effectuent les tâches réelles de chiffrement et de déchiffrement des données.

-   [Chiffrement de données](#encrypting-data-with-cng)
-   [Exemple de chiffrement de données](#encrypting-data-example)
-   [Déchiffrement de données](#decrypting-data)

## <a name="encrypting-data"></a>Chiffrement de données

Pour chiffrer les données, procédez comme suit :

1.  Ouvrez un fournisseur d’algorithme qui prend en charge le chiffrement, tel que **BCRYPT \_ des \_ algorithmes**.
2.  Créez une clé avec laquelle chiffrer les données. Une clé peut être créée à l’aide de l’une des fonctions suivantes :
    -   [**BCryptGenerateKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratekeypair) ou [**BCryptImportKeyPair**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkeypair) pour les fournisseurs asymétriques.
    -   [**BCryptGenerateSymmetricKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey) ou [**BCryptImportKey**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptimportkey) pour les fournisseurs symétriques.

    > [!Note]  
    > Le chiffrement et le déchiffrement des données avec une clé asymétrique sont gourmands en calculs par rapport au chiffrement à clé symétrique. Si vous devez chiffrer les données avec une clé asymétrique, vous devez chiffrer les données avec une clé symétrique, chiffrer la clé symétrique avec une clé asymétrique et inclure la clé symétrique chiffrée avec le message. Le destinataire peut ensuite déchiffrer la clé symétrique et utiliser la clé symétrique pour déchiffrer les données.

     

3.  Obtenir la taille des données chiffrées. Cela est basé sur l’algorithme de chiffrement, le schéma de remplissage (le cas échéant) et la taille des données à chiffrer. Vous pouvez obtenir la taille des données chiffrées à l’aide de la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) , en transmettant la **valeur null** pour le paramètre *pbOutput* . Tous les autres paramètres doivent être les mêmes que lorsque les données sont réellement chiffrées, à l’exception du paramètre *pbInput* , qui n’est pas utilisé dans ce cas.
4.  Vous pouvez chiffrer les données sur place avec la même mémoire tampon ou chiffrer les données dans une mémoire tampon distincte.

    Si vous souhaitez chiffrer les données en place, transmettez le pointeur de mémoire tampon en texte clair pour les paramètres *pbInput* et *pbOutput* dans la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) . Il est possible que la taille des données chiffrées soit supérieure à la taille des données non chiffrées, de sorte que la mémoire tampon de texte en clair doit être suffisamment grande pour contenir les données chiffrées, pas seulement le texte en clair. Vous pouvez utiliser la taille obtenue à l’étape 3 pour allouer la mémoire tampon de texte en clair.

    Si vous souhaitez chiffrer les données dans une mémoire tampon distincte, allouez une mémoire tampon pour les données chiffrées à l’aide de la taille obtenue à l’étape 3.

5.  Appelez la fonction [**BCryptEncrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptencrypt) pour chiffrer les données. Cette fonction écrira les données chiffrées à l’emplacement fourni dans le paramètre *pbOutput* .
6.  Rendez les données chiffrées persistantes si nécessaire.
7.  Répétez les étapes 5 et 6 jusqu’à ce que toutes les données aient été chiffrées.

## <a name="encrypting-data-example"></a>Exemple de chiffrement de données

L’exemple suivant montre comment chiffrer des données avec CNG à l’aide de l’algorithme de chiffrement symétrique Advanced Encryption Standard.


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



## <a name="decrypting-data"></a>Déchiffrement de données

Pour déchiffrer des données, procédez comme suit :

1.  Ouvrez un fournisseur d’algorithme qui prend en charge le chiffrement, tel que **BCRYPT \_ des \_ algorithmes**.
2.  Obtenez la clé avec laquelle les données ont été chiffrées et utilisez cette clé pour obtenir un handle pour la clé.
3.  Obtenir la taille des données déchiffrées. Cela est basé sur l’algorithme de chiffrement, le schéma de remplissage (le cas échéant) et la taille des données à déchiffrer. Vous pouvez obtenir la taille des données chiffrées à l’aide de la fonction [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) , en transmettant la **valeur null** pour le paramètre *pbOutput* . Les paramètres qui spécifient le schéma de remplissage et le [*vecteur d’initialisation*](/windows/desktop/SecGloss/i-gly) (IV) doivent être les mêmes que lorsque les données ont été chiffrées, à l’exception du paramètre *pbInput* , qui n’est pas utilisé dans ce cas.
4.  Allouez une mémoire tampon pour les données déchiffrées.
5.  Vous pouvez déchiffrer les données en place à l’aide de la même mémoire tampon, ou déchiffrer les données dans une mémoire tampon distincte.

    Si vous souhaitez déchiffrer les données sur place, transmettez le pointeur de mémoire tampon de texte chiffré pour les paramètres *pbInput* et *pbOutput* dans la fonction [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) .

    Si vous souhaitez déchiffrer les données dans une mémoire tampon distincte, allouez une mémoire tampon pour les données déchiffrées à l’aide de la taille obtenue à l’étape 3.

6.  Appelez la fonction [**BCryptDecrypt**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdecrypt) pour déchiffrer les données. Les paramètres qui spécifient le modèle de remplissage et le vecteur d’alimentation doivent être les mêmes que lorsque les données ont été chiffrées. Cette fonction écrira les données déchiffrées à l’emplacement fourni dans le paramètre *pbOutput* .
7.  Rendez les données déchiffrées persistantes si nécessaire.
8.  Répétez les étapes 5 et 6 jusqu’à ce que toutes les données soient déchiffrées.

 

 
