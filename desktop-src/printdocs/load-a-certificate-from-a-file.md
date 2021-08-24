---
description: Cette rubrique décrit comment charger un certificat à partir d’un fichier de certificat.
ms.assetid: 60cced55-9fcc-4fce-a462-7abf3f4466f0
title: Charger un certificat à partir d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73161b133fec74478643baa8453421130b3f3ad18ff4e75429d79b3312919b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099093"
---
# <a name="load-a-certificate-from-a-file"></a>Charger un certificat à partir d’un fichier

Cette rubrique décrit comment charger un certificat à partir d’un fichier de certificat.

Pour charger un certificat à partir d’un fichier de certificat

1.  Ouvrez le fichier de certificat pour l’accès en lecture.
2.  Lisez le contenu du fichier de certificat dans la mémoire tampon du certificat.
3.  Créez un certificat à l’aide du contenu de la mémoire tampon.


```C++
// In the interest of simplicity, this example
//  uses a fixed-length buffer to hold the certificate. 
// A more robust solution would be to query the size
//  of the certificate file and dynamically
//  allocate a buffer of that size or greater.
#define CERTIFICATE_BUFFER_SIZE 1024

HRESULT  hr                  = S_OK;
BYTE     certEncoded[CERTIFICATE_BUFFER_SIZE] = {0};
DWORD    certEncodedSize     = 0L;
HANDLE   certFileHandle      = NULL;
BOOL     result              = FALSE;

// open the certificate file
certFileHandle = CreateFile(certFile, 
    GENERIC_READ, 
    0, 
    NULL, 
    OPEN_EXISTING, 
    FILE_ATTRIBUTE_NORMAL, 
    NULL);
if (INVALID_HANDLE_VALUE == certFileHandle) {
    hr = HRESULT_FROM_WIN32(GetLastError());
}

if (SUCCEEDED(hr)) {
    // if the buffer is large enough
    //  read the certificate file into the buffer
    if (GetFileSize (certFileHandle, NULL) <= CERTIFICATE_BUFFER_SIZE) {
        result = ReadFile(certFileHandle, 
            certEncoded, 
            CERTIFICATE_BUFFER_SIZE, 
            &certEncodedSize, 
            NULL);
        if (!result) {
            // the read failed, return the error as an HRESULT
            hr = HRESULT_FROM_WIN32(GetLastError());
        } else {
            hr = S_OK;
        }
    } else {
        // The certificate file is larger than the allocated buffer.
        //  To handle this error, you could dynamically allocate
        //  the certificate buffer based on the file size returned or 
        //  use a larger static buffer.
        hr = HRESULT_FROM_WIN32(ERROR_MORE_DATA);
    }    
}
if (SUCCEEDED(hr))
{
    // create a certificate from the contents of the buffer
    *cert = CertCreateCertificateContext(X509_ASN_ENCODING, 
        certEncoded, 
        certEncodedSize);
    if (!(*cert)) {
        hr = HRESULT_FROM_WIN32(GetLastError());
        CloseHandle(certFileHandle);
        hr = E_FAIL;
    } else {
        hr = S_OK;
    }
}
// close the certificate file
if (NULL != certFileHandle) CloseHandle(certFileHandle);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Vérifier qu’un certificat prend en charge une méthode de signature](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Utilisé dans cet exemple**
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[**CertCreateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
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

 

 
