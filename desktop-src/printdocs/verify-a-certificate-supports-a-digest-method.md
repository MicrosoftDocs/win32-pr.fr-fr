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
# <a name="verify-the-system-supports-a-digest-method"></a>Vérifier que le système prend en charge une méthode Digest

Cette rubrique explique comment vérifier que le système prend en charge une méthode Digest.

Les signatures numériques XPS utilisent l’API crypto, qui fournit des méthodes pour vérifier que le système prend en charge une méthode Digest spécifique. Pour utiliser la fonction **CryptXmlEnumAlgorithmInfo** de l’API crypto pour énumérer les méthodes de chiffrement prises en charge par le système, l’appelant doit fournir une méthode de rappel et une structure de données. La fonction **CryptXmlEnumAlgorithmInfo** passe les données d’énumération à l’appelant par le biais de la méthode de rappel.

La structure de données utilisée dans cet exemple est illustrée dans l’exemple de code suivant et contient les champs suivants :

| Champ                            | Description                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userDigestAlgorithm**          | Champ **LPWStr** qui pointe vers la chaîne qui contient l’URI de l’algorithme Digest à vérifier. |
| **userDigestAlgorithmSupported** | Valeur **booléenne** qui indique si l’algorithme Digest est pris en charge par le certificat.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



La méthode de l’API crypto qui énumère les méthodes Digest utilise une méthode de rappel pour retourner les données à l’appelant. **CryptXmlEnumAlgorithmInfo** énumère les méthodes de chiffrement prises en charge par le système et appelle la méthode de rappel pour chaque méthode Digest qu’il énumère, jusqu’à ce que la méthode de rappel retourne la **valeur false** ou jusqu’à ce que toutes les méthodes de synthèse prises en charge par le système soient énumérées. La méthode de rappel dans cet exemple compare la méthode Digest qui est passée par **CryptXmlEnumAlgorithmInfo** à la méthode Digest fournie par la méthode d’appel.


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



L’exemple de code suivant encapsule la fonctionnalité de validation dans une méthode unique, qui retourne une valeur **booléenne** qui indique si le système prend en charge la méthode Digest.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Charger un certificat à partir d’un fichier](load-a-certificate-from-a-file.md)
</dt> <dt>

[Vérifier qu’un certificat prend en charge une méthode de signature](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Utilisé dans cet exemple**
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

 

 
