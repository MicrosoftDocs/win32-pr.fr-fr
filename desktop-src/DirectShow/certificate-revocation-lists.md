---
description: Listes de révocation de certificat
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Listes de révocation de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234282"
---
# <a name="certificate-revocation-lists"></a>Listes de révocation de certificat

Cette rubrique explique comment examiner la liste de révocation de certificats (CRL) pour les pilotes révoqués lors de l’utilisation du protocole COPP (Certified Output Protection Protocol).

La liste de révocation de certificats contient des résumés de certificats révoqués et peut être fournie et signée uniquement par Microsoft. La liste de révocation des certificats est distribuée via des licences DRM (Digital Rights Management). La liste de révocation de certificats peut révoquer n’importe quel certificat dans la chaîne de certificats du pilote. Si un certificat de la chaîne est révoqué, ce certificat et tous les certificats situés au-dessous de lui dans la chaîne sont également révoqués.

pour récupérer la liste de révocation de certificats, l’application doit utiliser le kit de développement logiciel (SDK) Windows Media Format, version 9 ou ultérieure, et effectuer les étapes suivantes :

1.  appelez **WMCreateReader** pour créer Windows l’objet Media Format SDK reader.
2.  Interrogez l’objet lecteur de l’interface **IWMDRMReader** .
3.  Appelez **IWMDRMReader :: GetDRMProperty** avec la valeur g \_ wszWMDRMNet \_ Revocation pour obtenir la liste de révocation de certificats. Vous devez appeler cette méthode deux fois : une fois pour récupérer la taille de la mémoire tampon à allouer, et une fois pour remplir la mémoire tampon. Le deuxième appel retourne une chaîne qui contient la liste de révocation de certificats. La chaîne entière est encodée en base-64.
4.  Décodez la chaîne codée en base 64. Pour ce faire, vous pouvez utiliser la fonction **CryptStringToBinary** . Cette fonction fait partie de CryptoAPI.

> [!Note]  
> Pour utiliser l’interface **IWMDRMReader** , vous devez obtenir une bibliothèque DRM statique auprès de Microsoft et lier votre application à ce fichier de bibliothèque. pour plus d’informations, consultez la rubrique « obtention de la bibliothèque DRM requise » dans la documentation du kit de développement logiciel (SDK) Windows Media Format.

 

Si la liste de révocation de certificats n’est pas présente sur l’ordinateur de l’utilisateur, la méthode **GetDRMProperty** retourne la \_ propriété NS E DRM non \_ \_ prise en charge \_ . Actuellement, la seule façon d’obtenir la liste de révocation de certificats consiste à acquérir une licence DRM.

Le code suivant illustre une fonction qui retourne la liste de révocation de certificats :


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



Ensuite, l’application doit vérifier que la liste de révocation de certificats est valide. Pour ce faire, vérifiez que le certificat de liste de révocation de certificats, qui fait partie de la liste de révocation de certificats, est directement signé par le certificat racine Microsoft et que la valeur de l’élément SignCRL est définie sur 1. Vérifiez également la signature de la liste de révocation de certificats.

Une fois la liste de révocation de certificats vérifiée, l’application peut la stocker. Le numéro de version de la liste de révocation de certificats doit également être vérifié avant le stockage, afin que l’application stocke toujours la version la plus récente.

La liste de révocation de certificats a le format suivant.



| Section            | Contents                                                             |
|--------------------|----------------------------------------------------------------------|
| En-tête             | version32 : nombre d’entrées de la liste de révocation de certificats 32 bits                           |
| Entrées de révocation | Plusieurs entrées de révocation de 160 bits                                  |
| Certificat        | certificat lengthVariable-longueur de certificat 32                 |
| Signature          | signature 8 bits type16-bit signature lengthVariable-length signature |



 

> [!Note]  
> Toutes les valeurs entières sont non signées et sont représentées par une notation Big-endian (ordre d’octet réseau).

 

Descriptions des sections CRL

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Titre
</dt> <dd>

L’en-tête contient le numéro de version de la liste de révocation de certificats et le nombre d’entrées de révocation dans la liste de révocation de certificats. Une liste de révocation de certificats peut contenir zéro ou plusieurs entrées.

</dd> <dt>

<span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Entrées de révocation
</dt> <dd>

Chaque entrée de révocation est le condensé 160 bits d’un certificat révoqué. Comparez ce condensé avec l’élément DigestValue dans le certificat.

</dd> <dt>

<span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificat
</dt> <dd>

La section certificat contient une valeur 32 bits indiquant la longueur (en octets) du certificat XML et de sa chaîne de certificats, ainsi qu’un tableau d’octets contenant à la fois le certificat XML de l’autorité de certification et la chaîne de certificats qui contient Microsoft comme racine. Le certificat doit être signé par une autorité de certification habilitée à émettre des listes de révocation de certificats.

> [!Note]  
> Le certificat ne doit pas se terminer par un caractère null.

 

</dd> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature
</dt> <dd>

La section signature contient le type et la longueur de la signature, ainsi que la signature numérique elle-même. Le type 8 bits a la valeur 2 pour indiquer qu’il utilise SHA-1 avec le chiffrement RSA 1024 bits. La longueur est une valeur de 16 bits contenant la longueur de la signature numérique, en octets. La signature numérique est calculée sur toutes les sections précédentes de la liste de révocation de certificats.

La signature est calculée à l’aide du schéma de signature numérique RSASSA-PSS défini dans PKCS \# 1 (version 2,1). La fonction de hachage est SHA-1, qui est définie dans normes FIPS (Federal Information Processing Standard) (FIPS) 180-2, et la fonction de génération de masque est MGF1, qui est définie dans la section B. 2.1 dans PKCS \# 1 (version 2,1). Les opérations RSASP1 et RSAVP1 utilisent RSA avec un module 1024 bits avec un exposant de vérification de 65537.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



