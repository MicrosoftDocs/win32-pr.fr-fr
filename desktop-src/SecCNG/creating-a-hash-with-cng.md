---
description: Les hachages sont particulièrement utiles pour vérifier l’intégrité des données lorsqu’elles sont utilisées avec un algorithme de signature asymétrique.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Création d’un hachage avec CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013668"
---
# <a name="creating-a-hash-with-cng"></a>Création d’un hachage avec CNG

Un [*hachage*](/windows/desktop/SecGloss/h-gly) est une opération unidirectionnelle qui est effectuée sur un bloc de données pour créer une valeur de hachage unique qui représente le contenu des données. Quel que soit le moment où le hachage est exécuté, le même [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) effectué sur les mêmes données produira toujours la même valeur de hachage. Si l’une des données est modifiée, la valeur de hachage change de manière appropriée.

Les hachages ne sont pas utiles pour chiffrer les données, car ils ne sont pas destinés à être utilisés pour reproduire les données d’origine à partir de la valeur de hachage. Les hachages sont particulièrement utiles pour vérifier l’intégrité des données lorsqu’elles sont utilisées avec un algorithme de signature asymétrique. Par exemple, si vous avez haché un message texte, signé le hachage et inclus la valeur de hachage signée avec le message d’origine, le destinataire peut vérifier le hachage signé, créer la valeur de hachage pour le message reçu, puis comparer cette valeur de hachage à la valeur de hachage signée incluse dans le message d’origine. Si les deux valeurs de hachage sont identiques, le destinataire peut être raisonnablement sûr que le message d’origine n’a pas été modifié.

La taille de la valeur de hachage est fixe pour un algorithme de hachage particulier. Cela signifie que, quelle que soit la taille du bloc de données, la valeur de hachage est toujours de la même taille. Par exemple, l’algorithme de hachage SHA256 a une taille de valeur de hachage de 256 bits.

-   [Création d’un objet de hachage](#creating-a-hashing-object)
-   [Création d’un objet de hachage réutilisable](#creating-a-reusable-hashing-object)
-   [Duplication d’un objet de hachage](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a>Création d’un objet de hachage

Pour créer un hachage à l’aide de CNG, procédez comme suit :

1.  Ouvrez un fournisseur d’algorithme qui prend en charge l’algorithme souhaité. Les algorithmes de hachage classiques incluent MD2, MD4, MD5, SHA-1 et SHA256. Appelez la fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) et spécifiez l’identificateur d’algorithme approprié dans le paramètre *pszAlgId* . La fonction retourne un handle au fournisseur.
2.  Pour créer l’objet de hachage, procédez comme suit :

    1.  Obtenez la taille de l’objet en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour récupérer la propriété de longueur de l' **\_ objet \_ BCRYPT** .
    2.  Allouez de la mémoire pour contenir l’objet de hachage.
    3.  Créez l’objet en appelant la fonction [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .

3.  Hachez les données. Cela implique d’appeler la fonction [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) une ou plusieurs fois. Chaque appel ajoute les données spécifiées au hachage.
4.  Pour obtenir la valeur de hachage, procédez comme suit :

    1.  Récupérez la taille de la valeur en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour obtenir la propriété de **\_ \_ longueur de hachage BCRYPT** .
    2.  Allouez de la mémoire pour contenir la valeur.
    3.  Récupérez la valeur de hachage en appelant la fonction [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) . Une fois que cette fonction a été appelée, l’objet de hachage n’est plus valide.

5.  Pour effectuer cette procédure, vous devez effectuer les étapes de nettoyage suivantes :

    1.  Fermez l’objet de hachage en passant le descripteur de hachage à la fonction [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Libérez la mémoire que vous avez allouée pour l’objet de hachage.
    3.  Si vous ne créez pas d’autres objets de hachage, fermez le fournisseur d’algorithme en passant le descripteur de fournisseur à la fonction [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .

        Si vous créez davantage d’objets de hachage, nous vous suggérons de réutiliser le fournisseur d’algorithmes plutôt que de créer et de détruire plusieurs fois le même type de fournisseur d’algorithme.

    4.  Une fois que vous avez fini d’utiliser la mémoire de valeur de hachage, libérez-la.

L’exemple suivant montre comment créer une valeur de hachage à l’aide de CNG.


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved.
/*++

Abstract:

    Sample program for SHA 256 hashing using CNG

--*/


#include <windows.h>
#include <stdio.h>
#include <bcrypt.h>



#define NT_SUCCESS(Status)          (((NTSTATUS)(Status)) >= 0)

#define STATUS_UNSUCCESSFUL         ((NTSTATUS)0xC0000001L)


static const BYTE rgbMsg[] = 
{
    0x61, 0x62, 0x63
};


void __cdecl wmain(
                   int                      argc, 
                   __in_ecount(argc) LPWSTR *wargv)
{

    BCRYPT_ALG_HANDLE       hAlg            = NULL;
    BCRYPT_HASH_HANDLE      hHash           = NULL;
    NTSTATUS                status          = STATUS_UNSUCCESSFUL;
    DWORD                   cbData          = 0,
                            cbHash          = 0,
                            cbHashObject    = 0;
    PBYTE                   pbHashObject    = NULL;
    PBYTE                   pbHash          = NULL;

    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(wargv);

    //open an algorithm handle
    if(!NT_SUCCESS(status = BCryptOpenAlgorithmProvider(
                                                &hAlg,
                                                BCRYPT_SHA256_ALGORITHM,
                                                NULL,
                                                0)))
    {
        wprintf(L"**** Error 0x%x returned by BCryptOpenAlgorithmProvider\n", status);
        goto Cleanup;
    }

    //calculate the size of the buffer to hold the hash object
    if(!NT_SUCCESS(status = BCryptGetProperty(
                                        hAlg, 
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
                                        hAlg, 
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
                                        hAlg, 
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

    wprintf(L"Success!\n");

Cleanup:

    if(hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg,0);
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

}

```



## <a name="creating-a-reusable-hashing-object"></a>Création d’un objet de hachage réutilisable

à partir de Windows 8 et Windows Server 2012, vous pouvez créer un objet de hachage réutilisable pour les scénarios qui nécessitent le calcul de plusieurs hachages ou hmac en succession rapide. Pour ce faire, spécifiez l' **\_ \_ \_ indicateur de hachage de hachage BCRYPT** lors de l’appel de la fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) . Tous les fournisseurs d’algorithmes de hachage Microsoft prennent en charge cet indicateur. Un objet de hachage créé à l’aide de cet indicateur peut être réutilisé immédiatement après l’appel de [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) comme s’il avait été créé récemment en appelant [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash). Pour créer un objet de hachage réutilisable, procédez comme suit :

1.  Ouvrez un fournisseur d’algorithme qui prend en charge l’algorithme de hachage souhaité. Appelez la fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) et spécifiez l’identificateur d’algorithme approprié dans le paramètre *pszAlgId* et l' **\_ \_ \_ indicateur de réutilisabilité de hachage BCRYPT** dans le paramètre *dwFlags* . La fonction retourne un handle au fournisseur.
2.  Pour créer l’objet de hachage, procédez comme suit :

    1.  Obtenez la taille de l’objet en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour récupérer la propriété de longueur de l' **\_ objet \_ BCRYPT** .
    2.  Allouez de la mémoire pour contenir l’objet de hachage.
    3.  Créez l’objet en appelant la fonction [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Spécifiez l' **\_ \_ \_ indicateur de réutilisabilité de hachage BCRYPT** dans le paramètre *dwFlags* .

3.  Hachez les données en appelant la fonction [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .
4.  Pour obtenir la valeur de hachage, procédez comme suit :

    1.  Obtenez la taille de la valeur de hachage en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour obtenir la propriété de **\_ \_ longueur de hachage BCRYPT** .
    2.  Allouez de la mémoire pour contenir la valeur.
    3.  Récupérez la valeur de hachage en appelant [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).

5.  Pour réutiliser l’objet de hachage avec les nouvelles données, passez à l’étape 3.
6.  Pour effectuer cette procédure, vous devez effectuer les étapes de nettoyage suivantes :

    1.  Fermez l’objet de hachage en passant le descripteur de hachage à la fonction [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .
    2.  Libérez la mémoire que vous avez allouée pour l’objet de hachage.
    3.  Si vous ne créez pas d’autres objets de hachage, fermez le fournisseur d’algorithme en passant le descripteur de fournisseur à la fonction [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .
    4.  Une fois que vous avez fini d’utiliser la mémoire de valeur de hachage, libérez-la.

## <a name="duplicating-a-hash-object"></a>Duplication d’un objet de hachage

Dans certains cas, il peut être utile de hacher une certaine quantité de données communes, puis de créer deux objets de hachage distincts à partir des données communes. Vous n’avez pas à créer deux objets de hachage distincts et à hacher les données communes deux fois pour effectuer cette opération. Vous pouvez créer un objet de hachage unique et ajouter toutes les données communes à l’objet de hachage. Ensuite, vous pouvez utiliser la fonction [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) pour créer un doublon de l’objet de hachage d’origine. L’objet Hash dupliqué contient les mêmes informations d’État et les mêmes données hachées que l’objet d’origine, mais il s’agit d’un objet de hachage entièrement indépendant. Vous pouvez maintenant ajouter les données uniques à chacun des objets de hachage et obtenir la valeur de hachage comme indiqué dans l’exemple. Cette technique est utile lors du hachage d’un grand nombre de données communes. Il vous suffit d’ajouter les données communes au hachage d’origine une seule fois, puis vous pouvez dupliquer l’objet de hachage pour obtenir un objet de hachage unique.

 

 
