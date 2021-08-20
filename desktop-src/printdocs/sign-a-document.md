---
description: Cette rubrique décrit comment signer un document XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Signer un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef544b2c34af19282d697676d22903948355d23e18e1c646df691c720052cc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033877"
---
# <a name="sign-a-document"></a>Signer un document

Cette rubrique décrit comment signer un document XPS.

Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).

Pour signer un document XPS, commencez par le charger dans un gestionnaire de signature, comme décrit dans [initialiser le gestionnaire de signatures](initialize-the-signature-manager.md).

Pour signer un document qui a été chargé dans un gestionnaire de signature :

1.  Instanciez une interface [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .
2.  Définissez la stratégie de signature.
3.  Définissez la méthode de signature. Les constantes de chaîne d’URI de méthode de signature sont définies dans cryptxml. h. Pour plus d’informations sur les valeurs de méthode de signature valides, consultez [**IXpsSigningOptions :: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).
4.  Définissez la méthode Digest. Les constantes de chaîne d’URI de méthode Digest sont définies dans cryptxml. h. Pour plus d’informations sur les valeurs de méthode Digest valides, consultez [**IXpsSigningOptions :: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).
5.  Chargez le certificat comme décrit dans [charger un certificat à partir d’un fichier](load-a-certificate-from-a-file.md).
6.  Vérifiez que le certificat prend en charge la méthode de signature, comme décrit dans [vérifier qu’un certificat prend en charge une méthode de signature](verify-a-certificate-supports-a-signature-method.md).
7.  Vérifiez que la méthode Digest est prise en charge par le système, comme décrit dans [vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md).
8.  Si nécessaire, incorporez les certificats de la chaîne d’approbation de certificat dans le document XPS comme décrit dans [incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md).
9.  Signez le document XPS.

L’exemple de code suivant illustre l’utilisation des étapes précédentes dans un programme.


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Next Steps**
</dt> <dt>

[Ajouter une demande de signature à un document XPS](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Vérifier les signatures de document](verify-document-signatures.md)
</dt> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::CreateSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**IXpsSignatureManager :: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**IXpsSigningOptions::SetPolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**\_stratégie de signature XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[API de chiffrement](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Fonctions de chiffrement](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Charger un certificat à partir d’un fichier](load-a-certificate-from-a-file.md)
</dt> <dt>

[Vérifier qu’un certificat prend en charge une méthode de signature](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[Erreurs de l’API de signature numérique XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erreurs de document XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
