---
description: Cette rubrique explique comment vérifier qu’un certificat prend en charge une méthode de signature spécifique.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Vérifier qu’un certificat prend en charge une méthode de signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177859dd78d30ee9f9147cee7ca01311ed95c0733115cd939dde8aa6ec70f5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098711"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Vérifier qu’un certificat prend en charge une méthode de signature

Cette rubrique explique comment vérifier qu’un certificat prend en charge une méthode de signature spécifique.

Le **CryptXmlEnumAlgorithmInfo** dans l’API de chiffrement Microsoft énumère les propriétés d’un certificat et est utilisé dans cet exemple de code pour énumérer les méthodes de signature que le certificat prend en charge. Pour utiliser **CryptXmlEnumAlgorithmInfo** afin d’énumérer les méthodes de signature que le certificat prend en charge, l’appelant doit fournir une méthode de rappel et une structure de données dans l’appel à **CryptXmlEnumAlgorithmInfo**, ce qui lui permet de passer des données à la méthode de rappel.

La structure de données utilisée dans l’exemple de code suivant contient les champs suivants :

| Champ                               | Description                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **userSignatureAlgorithmToCheck**   | Champ **LPWStr** qui pointe vers la chaîne qui contient l’URI de l’algorithme de signature à vérifier.                             |
| **certificateAlgorithmInfo**        | Pointeur vers une structure **d' \_ \_ informations d’OID** de chiffrement qui contient des informations sur un algorithme de signature qui est pris en charge par le certificat. |
| **userSignatureAlgorithmSupported** | Valeur **booléenne** qui indique si l’algorithme de signature est pris en charge par le certificat.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



La méthode de l’API crypto qui vérifie le certificat utilise une méthode de rappel pour retourner les données à l’appelant. **CryptXmlEnumAlgorithmInfo** énumère les méthodes de signature que le certificat prend en charge et appelle la méthode de rappel pour chaque méthode de signature jusqu’à ce que la méthode de rappel retourne la **valeur false** ou jusqu’à ce que toutes les méthodes de signature du certificat aient été énumérées.

La méthode de rappel dans l’exemple de code suivant recherche une méthode de signature passée par **CryptXmlEnumAlgorithmInfo** qui correspond à la méthode de signature fournie par la méthode d’appel. Lorsqu’une correspondance est trouvée, la méthode de rappel vérifie si la méthode de signature est également prise en charge par le système. Si les méthodes de signature correspondent et sont prises en charge par le système, la méthode de signature est marquée comme étant prise en charge par le système et la méthode de rappel retourne **false**.


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



L’exemple de code suivant encapsule la fonctionnalité de validation dans une méthode unique. Cette méthode retourne une valeur **booléenne** qui indique si le certificat prend en charge la méthode de signature et si la méthode de signature est prise en charge par le système.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Charger un certificat à partir d’un fichier](load-a-certificate-from-a-file.md)
</dt> <dt>

[Vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Utilisé dans cet exemple**
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**\_informations d’OID de chiffre \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[API de chiffrement](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Fonctions de chiffrement](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Erreurs de l’API de signature numérique XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erreurs de document XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
