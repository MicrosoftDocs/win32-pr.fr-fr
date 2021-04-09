---
description: Cette rubrique explique comment vérifier qu’un certificat prend en charge une méthode de signature spécifique.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Vérifier qu’un certificat prend en charge une méthode de signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868013"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="da28d-103">Vérifier qu’un certificat prend en charge une méthode de signature</span><span class="sxs-lookup"><span data-stu-id="da28d-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="da28d-104">Cette rubrique explique comment vérifier qu’un certificat prend en charge une méthode de signature spécifique.</span><span class="sxs-lookup"><span data-stu-id="da28d-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="da28d-105">Le **CryptXmlEnumAlgorithmInfo** dans l’API de chiffrement Microsoft énumère les propriétés d’un certificat et est utilisé dans cet exemple de code pour énumérer les méthodes de signature que le certificat prend en charge.</span><span class="sxs-lookup"><span data-stu-id="da28d-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="da28d-106">Pour utiliser **CryptXmlEnumAlgorithmInfo** afin d’énumérer les méthodes de signature que le certificat prend en charge, l’appelant doit fournir une méthode de rappel et une structure de données dans l’appel à **CryptXmlEnumAlgorithmInfo**, ce qui lui permet de passer des données à la méthode de rappel.</span><span class="sxs-lookup"><span data-stu-id="da28d-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="da28d-107">La structure de données utilisée dans l’exemple de code suivant contient les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="da28d-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="da28d-108">Champ</span><span class="sxs-lookup"><span data-stu-id="da28d-108">Field</span></span>                               | <span data-ttu-id="da28d-109">Description</span><span class="sxs-lookup"><span data-stu-id="da28d-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da28d-110">**userSignatureAlgorithmToCheck**</span><span class="sxs-lookup"><span data-stu-id="da28d-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="da28d-111">Champ **LPWStr** qui pointe vers la chaîne qui contient l’URI de l’algorithme de signature à vérifier.</span><span class="sxs-lookup"><span data-stu-id="da28d-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="da28d-112">**certificateAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="da28d-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="da28d-113">Pointeur vers une structure **d' \_ \_ informations d’OID** de chiffrement qui contient des informations sur un algorithme de signature qui est pris en charge par le certificat.</span><span class="sxs-lookup"><span data-stu-id="da28d-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="da28d-114">**userSignatureAlgorithmSupported**</span><span class="sxs-lookup"><span data-stu-id="da28d-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="da28d-115">Valeur **booléenne** qui indique si l’algorithme de signature est pris en charge par le certificat.</span><span class="sxs-lookup"><span data-stu-id="da28d-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="da28d-116">La méthode de l’API crypto qui vérifie le certificat utilise une méthode de rappel pour retourner les données à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="da28d-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="da28d-117">**CryptXmlEnumAlgorithmInfo** énumère les méthodes de signature que le certificat prend en charge et appelle la méthode de rappel pour chaque méthode de signature jusqu’à ce que la méthode de rappel retourne la **valeur false** ou jusqu’à ce que toutes les méthodes de signature du certificat aient été énumérées.</span><span class="sxs-lookup"><span data-stu-id="da28d-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="da28d-118">La méthode de rappel dans l’exemple de code suivant recherche une méthode de signature passée par **CryptXmlEnumAlgorithmInfo** qui correspond à la méthode de signature fournie par la méthode d’appel.</span><span class="sxs-lookup"><span data-stu-id="da28d-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="da28d-119">Lorsqu’une correspondance est trouvée, la méthode de rappel vérifie si la méthode de signature est également prise en charge par le système.</span><span class="sxs-lookup"><span data-stu-id="da28d-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="da28d-120">Si les méthodes de signature correspondent et sont prises en charge par le système, la méthode de signature est marquée comme étant prise en charge par le système et la méthode de rappel retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="da28d-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



<span data-ttu-id="da28d-121">L’exemple de code suivant encapsule la fonctionnalité de validation dans une méthode unique.</span><span class="sxs-lookup"><span data-stu-id="da28d-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="da28d-122">Cette méthode retourne une valeur **booléenne** qui indique si le certificat prend en charge la méthode de signature et si la méthode de signature est prise en charge par le système.</span><span class="sxs-lookup"><span data-stu-id="da28d-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a><span data-ttu-id="da28d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da28d-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="da28d-124">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="da28d-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="da28d-125">Charger un certificat à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="da28d-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="da28d-126">Vérifier que le système prend en charge une méthode Digest</span><span class="sxs-lookup"><span data-stu-id="da28d-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="da28d-127">Incorporer des chaînes de certificats dans un document</span><span class="sxs-lookup"><span data-stu-id="da28d-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="da28d-128">**Utilisé dans cet exemple**</span><span class="sxs-lookup"><span data-stu-id="da28d-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="da28d-129">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="da28d-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="da28d-130">**\_informations d’OID de chiffre \_**</span><span class="sxs-lookup"><span data-stu-id="da28d-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="da28d-131">**CryptXmlEnumAlgorithmInfo**</span><span class="sxs-lookup"><span data-stu-id="da28d-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="da28d-132">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="da28d-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="da28d-133">API de chiffrement</span><span class="sxs-lookup"><span data-stu-id="da28d-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="da28d-134">Fonctions de chiffrement</span><span class="sxs-lookup"><span data-stu-id="da28d-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="da28d-135">Erreurs de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="da28d-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="da28d-136">Erreurs de document XPS</span><span class="sxs-lookup"><span data-stu-id="da28d-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="da28d-137">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="da28d-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
