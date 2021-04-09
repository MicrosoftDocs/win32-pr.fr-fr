---
description: Cette rubrique explique comment vérifier que le système prend en charge une méthode Digest.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Vérifier que le système prend en charge une méthode Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868014"
---
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="14318-103">Vérifier que le système prend en charge une méthode Digest</span><span class="sxs-lookup"><span data-stu-id="14318-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="14318-104">Cette rubrique explique comment vérifier que le système prend en charge une méthode Digest.</span><span class="sxs-lookup"><span data-stu-id="14318-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="14318-105">Les signatures numériques XPS utilisent l’API crypto, qui fournit des méthodes pour vérifier que le système prend en charge une méthode Digest spécifique.</span><span class="sxs-lookup"><span data-stu-id="14318-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="14318-106">Pour utiliser la fonction **CryptXmlEnumAlgorithmInfo** de l’API crypto pour énumérer les méthodes de chiffrement prises en charge par le système, l’appelant doit fournir une méthode de rappel et une structure de données.</span><span class="sxs-lookup"><span data-stu-id="14318-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="14318-107">La fonction **CryptXmlEnumAlgorithmInfo** passe les données d’énumération à l’appelant par le biais de la méthode de rappel.</span><span class="sxs-lookup"><span data-stu-id="14318-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="14318-108">La structure de données utilisée dans cet exemple est illustrée dans l’exemple de code suivant et contient les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="14318-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="14318-109">Champ</span><span class="sxs-lookup"><span data-stu-id="14318-109">Field</span></span>                            | <span data-ttu-id="14318-110">Description</span><span class="sxs-lookup"><span data-stu-id="14318-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14318-111">**userDigestAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="14318-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="14318-112">Champ **LPWStr** qui pointe vers la chaîne qui contient l’URI de l’algorithme Digest à vérifier.</span><span class="sxs-lookup"><span data-stu-id="14318-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="14318-113">**userDigestAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="14318-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="14318-114">Valeur **booléenne** qui indique si l’algorithme Digest est pris en charge par le certificat.</span><span class="sxs-lookup"><span data-stu-id="14318-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="14318-115">La méthode de l’API crypto qui énumère les méthodes Digest utilise une méthode de rappel pour retourner les données à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="14318-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="14318-116">**CryptXmlEnumAlgorithmInfo** énumère les méthodes de chiffrement prises en charge par le système et appelle la méthode de rappel pour chaque méthode Digest qu’il énumère, jusqu’à ce que la méthode de rappel retourne la **valeur false** ou jusqu’à ce que toutes les méthodes de synthèse prises en charge par le système soient énumérées.</span><span class="sxs-lookup"><span data-stu-id="14318-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="14318-117">La méthode de rappel dans cet exemple compare la méthode Digest qui est passée par **CryptXmlEnumAlgorithmInfo** à la méthode Digest fournie par la méthode d’appel.</span><span class="sxs-lookup"><span data-stu-id="14318-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



<span data-ttu-id="14318-118">L’exemple de code suivant encapsule la fonctionnalité de validation dans une méthode unique, qui retourne une valeur **booléenne** qui indique si le système prend en charge la méthode Digest.</span><span class="sxs-lookup"><span data-stu-id="14318-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
}
```



## <a name="related-topics"></a><span data-ttu-id="14318-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14318-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="14318-120">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="14318-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="14318-121">Charger un certificat à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="14318-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="14318-122">Vérifier qu’un certificat prend en charge une méthode de signature</span><span class="sxs-lookup"><span data-stu-id="14318-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="14318-123">Incorporer des chaînes de certificats dans un document</span><span class="sxs-lookup"><span data-stu-id="14318-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="14318-124">**Utilisé dans cet exemple**</span><span class="sxs-lookup"><span data-stu-id="14318-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="14318-125">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="14318-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="14318-126">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="14318-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="14318-127">API de chiffrement</span><span class="sxs-lookup"><span data-stu-id="14318-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="14318-128">Fonctions de chiffrement</span><span class="sxs-lookup"><span data-stu-id="14318-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="14318-129">Erreurs de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="14318-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="14318-130">Erreurs de document XPS</span><span class="sxs-lookup"><span data-stu-id="14318-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="14318-131">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="14318-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
