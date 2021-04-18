---
description: Les hachages sont particulièrement utiles pour vérifier l’intégrité des données lorsqu’elles sont utilisées avec un algorithme de signature asymétrique.
ms.assetid: f36b7e36-4377-4940-8951-6caba6e3ce8a
title: Création d’un hachage avec CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735f95182b63facee687f408ea4a07e09399e562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512919"
---
# <a name="creating-a-hash-with-cng"></a><span data-ttu-id="5db6d-103">Création d’un hachage avec CNG</span><span class="sxs-lookup"><span data-stu-id="5db6d-103">Creating a Hash with CNG</span></span>

<span data-ttu-id="5db6d-104">Un [*hachage*](/windows/desktop/SecGloss/h-gly) est une opération unidirectionnelle qui est effectuée sur un bloc de données pour créer une valeur de hachage unique qui représente le contenu des données.</span><span class="sxs-lookup"><span data-stu-id="5db6d-104">A [*hash*](/windows/desktop/SecGloss/h-gly) is a one way operation that is performed on a block of data to create a unique hash value that represents the contents of the data.</span></span> <span data-ttu-id="5db6d-105">Quel que soit le moment où le hachage est exécuté, le même [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) effectué sur les mêmes données produira toujours la même valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-105">No matter when the hash is performed, the same [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) performed on the same data will always produce the same hash value.</span></span> <span data-ttu-id="5db6d-106">Si l’une des données est modifiée, la valeur de hachage change de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="5db6d-106">If any of the data changes, the hash value will change appropriately.</span></span>

<span data-ttu-id="5db6d-107">Les hachages ne sont pas utiles pour chiffrer les données, car ils ne sont pas destinés à être utilisés pour reproduire les données d’origine à partir de la valeur de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-107">Hashes are not useful for encrypting data because they are not intended to be used to reproduce the original data from the hash value.</span></span> <span data-ttu-id="5db6d-108">Les hachages sont particulièrement utiles pour vérifier l’intégrité des données lorsqu’elles sont utilisées avec un algorithme de signature asymétrique.</span><span class="sxs-lookup"><span data-stu-id="5db6d-108">Hashes are most useful to verify the integrity of the data when used with an asymmetric signing algorithm.</span></span> <span data-ttu-id="5db6d-109">Par exemple, si vous avez haché un message texte, signé le hachage et inclus la valeur de hachage signée avec le message d’origine, le destinataire peut vérifier le hachage signé, créer la valeur de hachage pour le message reçu, puis comparer cette valeur de hachage à la valeur de hachage signée incluse dans le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="5db6d-109">For example, if you hashed a text message, signed the hash, and included the signed hash value with the original message, the recipient could verify the signed hash, create the hash value for the received message, and then compare this hash value with the signed hash value included with the original message.</span></span> <span data-ttu-id="5db6d-110">Si les deux valeurs de hachage sont identiques, le destinataire peut être raisonnablement sûr que le message d’origine n’a pas été modifié.</span><span class="sxs-lookup"><span data-stu-id="5db6d-110">If the two hash values are identical, the recipient can be reasonably sure that the original message has not been modified.</span></span>

<span data-ttu-id="5db6d-111">La taille de la valeur de hachage est fixe pour un algorithme de hachage particulier.</span><span class="sxs-lookup"><span data-stu-id="5db6d-111">The size of the hash value is fixed for a particular hashing algorithm.</span></span> <span data-ttu-id="5db6d-112">Cela signifie que, quelle que soit la taille du bloc de données, la valeur de hachage est toujours de la même taille.</span><span class="sxs-lookup"><span data-stu-id="5db6d-112">What this means is that no matter how large or small the data block is, the hash value will always be the same size.</span></span> <span data-ttu-id="5db6d-113">Par exemple, l’algorithme de hachage SHA256 a une taille de valeur de hachage de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="5db6d-113">As an example, the SHA256 hashing algorithm has a hash value size of 256 bits.</span></span>

-   [<span data-ttu-id="5db6d-114">Création d’un objet de hachage</span><span class="sxs-lookup"><span data-stu-id="5db6d-114">Creating a Hashing Object</span></span>](#creating-a-hashing-object)
-   [<span data-ttu-id="5db6d-115">Création d’un objet de hachage réutilisable</span><span class="sxs-lookup"><span data-stu-id="5db6d-115">Creating a Reusable Hashing Object</span></span>](#creating-a-reusable-hashing-object)
-   [<span data-ttu-id="5db6d-116">Duplication d’un objet de hachage</span><span class="sxs-lookup"><span data-stu-id="5db6d-116">Duplicating a Hash Object</span></span>](#duplicating-a-hash-object)

## <a name="creating-a-hashing-object"></a><span data-ttu-id="5db6d-117">Création d’un objet de hachage</span><span class="sxs-lookup"><span data-stu-id="5db6d-117">Creating a Hashing Object</span></span>

<span data-ttu-id="5db6d-118">Pour créer un hachage à l’aide de CNG, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5db6d-118">To create a hash using CNG, perform the following steps:</span></span>

1.  <span data-ttu-id="5db6d-119">Ouvrez un fournisseur d’algorithme qui prend en charge l’algorithme souhaité.</span><span class="sxs-lookup"><span data-stu-id="5db6d-119">Open an algorithm provider that supports the desired algorithm.</span></span> <span data-ttu-id="5db6d-120">Les algorithmes de hachage classiques incluent MD2, MD4, MD5, SHA-1 et SHA256.</span><span class="sxs-lookup"><span data-stu-id="5db6d-120">Typical hashing algorithms include MD2, MD4, MD5, SHA-1, and SHA256.</span></span> <span data-ttu-id="5db6d-121">Appelez la fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) et spécifiez l’identificateur d’algorithme approprié dans le paramètre *pszAlgId* .</span><span class="sxs-lookup"><span data-stu-id="5db6d-121">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter.</span></span> <span data-ttu-id="5db6d-122">La fonction retourne un handle au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5db6d-122">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="5db6d-123">Pour créer l’objet de hachage, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5db6d-123">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="5db6d-124">Obtenez la taille de l’objet en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour récupérer la propriété de longueur de l' **\_ objet \_ BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="5db6d-124">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="5db6d-125">Allouez de la mémoire pour contenir l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-125">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="5db6d-126">Créez l’objet en appelant la fonction [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-126">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span>

3.  <span data-ttu-id="5db6d-127">Hachez les données.</span><span class="sxs-lookup"><span data-stu-id="5db6d-127">Hash the data.</span></span> <span data-ttu-id="5db6d-128">Cela implique d’appeler la fonction [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) une ou plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="5db6d-128">This involves calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function one or more times.</span></span> <span data-ttu-id="5db6d-129">Chaque appel ajoute les données spécifiées au hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-129">Each call appends the specified data to the hash.</span></span>
4.  <span data-ttu-id="5db6d-130">Pour obtenir la valeur de hachage, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5db6d-130">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="5db6d-131">Récupérez la taille de la valeur en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour obtenir la propriété de **\_ \_ longueur de hachage BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="5db6d-131">Retrieve the size of the value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="5db6d-132">Allouez de la mémoire pour contenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="5db6d-132">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="5db6d-133">Récupérez la valeur de hachage en appelant la fonction [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-133">Retrieve the hash value by calling the [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) function.</span></span> <span data-ttu-id="5db6d-134">Une fois que cette fonction a été appelée, l’objet de hachage n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="5db6d-134">After this function has been called, the hash object is no longer valid.</span></span>

5.  <span data-ttu-id="5db6d-135">Pour effectuer cette procédure, vous devez effectuer les étapes de nettoyage suivantes :</span><span class="sxs-lookup"><span data-stu-id="5db6d-135">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="5db6d-136">Fermez l’objet de hachage en passant le descripteur de hachage à la fonction [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-136">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="5db6d-137">Libérez la mémoire que vous avez allouée pour l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-137">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="5db6d-138">Si vous ne créez pas d’autres objets de hachage, fermez le fournisseur d’algorithme en passant le descripteur de fournisseur à la fonction [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-138">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>

        <span data-ttu-id="5db6d-139">Si vous créez davantage d’objets de hachage, nous vous suggérons de réutiliser le fournisseur d’algorithmes plutôt que de créer et de détruire plusieurs fois le même type de fournisseur d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="5db6d-139">If you will be creating more hash objects, we suggest you reuse the algorithm provider rather than creating and destroying the same type of algorithm provider many times.</span></span>

    4.  <span data-ttu-id="5db6d-140">Une fois que vous avez fini d’utiliser la mémoire de valeur de hachage, libérez-la.</span><span class="sxs-lookup"><span data-stu-id="5db6d-140">When you have finished using the hash value memory, free it.</span></span>

<span data-ttu-id="5db6d-141">L’exemple suivant montre comment créer une valeur de hachage à l’aide de CNG.</span><span class="sxs-lookup"><span data-stu-id="5db6d-141">The following example shows how to create a hash value by using CNG.</span></span>


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



## <a name="creating-a-reusable-hashing-object"></a><span data-ttu-id="5db6d-142">Création d’un objet de hachage réutilisable</span><span class="sxs-lookup"><span data-stu-id="5db6d-142">Creating a Reusable Hashing Object</span></span>

<span data-ttu-id="5db6d-143">À compter de Windows 8 et de Windows Server 2012, vous pouvez créer un objet de hachage réutilisable pour les scénarios qui nécessitent le calcul de plusieurs hachages ou HMAC en succession rapide.</span><span class="sxs-lookup"><span data-stu-id="5db6d-143">Beginning with Windows 8 and Windows Server 2012, you can create a reusable hashing object for scenarios that require you to compute multiple hashes or HMACs in rapid succession.</span></span> <span data-ttu-id="5db6d-144">Pour ce faire, spécifiez l' **\_ \_ \_ indicateur de hachage de hachage BCRYPT** lors de l’appel de la fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-144">Do this by specifying the **BCRYPT\_HASH\_REUSABLE\_FLAG** when calling the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function.</span></span> <span data-ttu-id="5db6d-145">Tous les fournisseurs d’algorithmes de hachage Microsoft prennent en charge cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="5db6d-145">All Microsoft hash algorithm providers support this flag.</span></span> <span data-ttu-id="5db6d-146">Un objet de hachage créé à l’aide de cet indicateur peut être réutilisé immédiatement après l’appel de [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) comme s’il avait été créé récemment en appelant [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="5db6d-146">A hashing object created by using this flag can be reused immediately after calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash) just as if it had been freshly created by calling [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash).</span></span> <span data-ttu-id="5db6d-147">Pour créer un objet de hachage réutilisable, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5db6d-147">Perform the following steps to create a reusable hashing object:</span></span>

1.  <span data-ttu-id="5db6d-148">Ouvrez un fournisseur d’algorithme qui prend en charge l’algorithme de hachage souhaité.</span><span class="sxs-lookup"><span data-stu-id="5db6d-148">Open an algorithm provider that supports the desired hashing algorithm.</span></span> <span data-ttu-id="5db6d-149">Appelez la fonction [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) et spécifiez l’identificateur d’algorithme approprié dans le paramètre *pszAlgId* et l' **\_ \_ \_ indicateur de réutilisabilité de hachage BCRYPT** dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="5db6d-149">Call the [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) function and specify the appropriate algorithm identifier in the *pszAlgId* parameter and **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span> <span data-ttu-id="5db6d-150">La fonction retourne un handle au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5db6d-150">The function returns a handle to the provider.</span></span>
2.  <span data-ttu-id="5db6d-151">Pour créer l’objet de hachage, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5db6d-151">Perform the following steps to create the hashing object:</span></span>

    1.  <span data-ttu-id="5db6d-152">Obtenez la taille de l’objet en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour récupérer la propriété de longueur de l' **\_ objet \_ BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="5db6d-152">Obtain the size of the object by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to retrieve the **BCRYPT\_OBJECT\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="5db6d-153">Allouez de la mémoire pour contenir l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-153">Allocate memory to hold the hash object.</span></span>
    3.  <span data-ttu-id="5db6d-154">Créez l’objet en appelant la fonction [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-154">Create the object by calling the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="5db6d-155">Spécifiez l' **\_ \_ \_ indicateur de réutilisabilité de hachage BCRYPT** dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="5db6d-155">Specify **BCRYPT\_HASH\_REUSABLE\_FLAG** in the *dwFlags* parameter.</span></span>

3.  <span data-ttu-id="5db6d-156">Hachez les données en appelant la fonction [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-156">Hash the data by calling the [**BCryptHashData**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcrypthashdata) function.</span></span>
4.  <span data-ttu-id="5db6d-157">Pour obtenir la valeur de hachage, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="5db6d-157">Perform the following steps to obtain the hash value:</span></span>

    1.  <span data-ttu-id="5db6d-158">Obtenez la taille de la valeur de hachage en appelant la fonction [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) pour obtenir la propriété de **\_ \_ longueur de hachage BCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="5db6d-158">Obtain the size of the hash value by calling the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) function to get the **BCRYPT\_HASH\_LENGTH** property.</span></span>
    2.  <span data-ttu-id="5db6d-159">Allouez de la mémoire pour contenir la valeur.</span><span class="sxs-lookup"><span data-stu-id="5db6d-159">Allocate memory to hold the value.</span></span>
    3.  <span data-ttu-id="5db6d-160">Récupérez la valeur de hachage en appelant [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span><span class="sxs-lookup"><span data-stu-id="5db6d-160">Get the hash value by calling [**BCryptFinishHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptfinishhash).</span></span>

5.  <span data-ttu-id="5db6d-161">Pour réutiliser l’objet de hachage avec les nouvelles données, passez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="5db6d-161">To reuse the hashing object with new data, go to step 3.</span></span>
6.  <span data-ttu-id="5db6d-162">Pour effectuer cette procédure, vous devez effectuer les étapes de nettoyage suivantes :</span><span class="sxs-lookup"><span data-stu-id="5db6d-162">To complete this procedure, you must perform the following cleanup steps:</span></span>

    1.  <span data-ttu-id="5db6d-163">Fermez l’objet de hachage en passant le descripteur de hachage à la fonction [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-163">Close the hash object by passing the hash handle to the [**BCryptDestroyHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptdestroyhash) function.</span></span>
    2.  <span data-ttu-id="5db6d-164">Libérez la mémoire que vous avez allouée pour l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-164">Free the memory you allocated for the hash object.</span></span>
    3.  <span data-ttu-id="5db6d-165">Si vous ne créez pas d’autres objets de hachage, fermez le fournisseur d’algorithme en passant le descripteur de fournisseur à la fonction [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) .</span><span class="sxs-lookup"><span data-stu-id="5db6d-165">If you will not be creating any more hash objects, close the algorithm provider by passing the provider handle to the [**BCryptCloseAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptclosealgorithmprovider) function.</span></span>
    4.  <span data-ttu-id="5db6d-166">Une fois que vous avez fini d’utiliser la mémoire de valeur de hachage, libérez-la.</span><span class="sxs-lookup"><span data-stu-id="5db6d-166">When you have finished using the hash value memory, free it.</span></span>

## <a name="duplicating-a-hash-object"></a><span data-ttu-id="5db6d-167">Duplication d’un objet de hachage</span><span class="sxs-lookup"><span data-stu-id="5db6d-167">Duplicating a Hash Object</span></span>

<span data-ttu-id="5db6d-168">Dans certains cas, il peut être utile de hacher une certaine quantité de données communes, puis de créer deux objets de hachage distincts à partir des données communes.</span><span class="sxs-lookup"><span data-stu-id="5db6d-168">In some circumstances, it may be useful to hash some amount of common data and then create two separate hash objects from the common data.</span></span> <span data-ttu-id="5db6d-169">Vous n’avez pas à créer deux objets de hachage distincts et à hacher les données communes deux fois pour effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="5db6d-169">You do not have to create two separate hash objects and hash the common data twice to accomplish this.</span></span> <span data-ttu-id="5db6d-170">Vous pouvez créer un objet de hachage unique et ajouter toutes les données communes à l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="5db6d-170">You can create a single hash object and add all of the common data to the hash object.</span></span> <span data-ttu-id="5db6d-171">Ensuite, vous pouvez utiliser la fonction [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) pour créer un doublon de l’objet de hachage d’origine.</span><span class="sxs-lookup"><span data-stu-id="5db6d-171">Then, you can use the [**BCryptDuplicateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptduplicatehash) function to create a duplicate of the original hash object.</span></span> <span data-ttu-id="5db6d-172">L’objet Hash dupliqué contient les mêmes informations d’État et les mêmes données hachées que l’objet d’origine, mais il s’agit d’un objet de hachage entièrement indépendant.</span><span class="sxs-lookup"><span data-stu-id="5db6d-172">The duplicate hash object contains all of the same state information and hashed data as the original, but it is a completely independent hash object.</span></span> <span data-ttu-id="5db6d-173">Vous pouvez maintenant ajouter les données uniques à chacun des objets de hachage et obtenir la valeur de hachage comme indiqué dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5db6d-173">You can now add the unique data to each of the hash objects and obtain the hash value as shown in the example.</span></span> <span data-ttu-id="5db6d-174">Cette technique est utile lors du hachage d’un grand nombre de données communes.</span><span class="sxs-lookup"><span data-stu-id="5db6d-174">This technique is useful when hashing a possibly large amount of common data.</span></span> <span data-ttu-id="5db6d-175">Il vous suffit d’ajouter les données communes au hachage d’origine une seule fois, puis vous pouvez dupliquer l’objet de hachage pour obtenir un objet de hachage unique.</span><span class="sxs-lookup"><span data-stu-id="5db6d-175">You only have to add the common data to the original hash one time, and then you can duplicate the hash object to obtain a unique hash object.</span></span>

 

 
