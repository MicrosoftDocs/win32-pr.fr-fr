---
description: Cette rubrique explique comment incorporer les certificats qui composent une chaîne de certificats dans un document XPS.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Incorporer des chaînes de certificats dans un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23e47b4cd0d140d7200fb8aa01642ea5fbb731e49dcc289f596a054b0accbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447579"
---
# <a name="embed-certificate-chains-in-a-document"></a>Incorporer des chaînes de certificats dans un document

Cette rubrique explique comment incorporer les certificats qui composent une chaîne de certificats dans un document XPS. Une chaîne de certificats se compose de tous les certificats, à l’exception du certificat racine, qui sont nécessaires pour certifier le sujet identifié par le certificat de fin.

Pour incorporer une chaîne de certificat dans un document XPS, commencez par créer la chaîne de certificats, comme illustré dans l’exemple de code suivant.

La méthode **CreateCertificateChain** dans l’exemple de code accepte *certificateStore* en tant que paramètre, qui est une valeur **HCERTSTORE** . Si cette valeur est **null**, les certificats sont récupérés à partir du serveur de certificats de l’ordinateur client. Si la valeur est le descripteur d’un magasin de certificats, les certificats sont récupérés à partir de ce magasin référencé par *certificateStore* , ainsi qu’à partir du serveur de certificats de l’ordinateur client.


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



L’exemple de code suivant crée une chaîne de certificats à partir de certificats, puis ajoute ces certificats à un document XPS. Notez que [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) crée la chaîne de certificats dans laquelle le certificat de signature est tout d’abord et le certificat racine est le dernier. Le certificat de signature et le certificat racine ne sont pas ajoutés dans cet exemple. Les certificats de signature sont ajoutés à l’aide d’un appel à la méthode [**IXpsSignatureManager :: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) , qui doit être la dernière méthode de signature appelée sur le document. Le certificat racine n’est pas ajouté lorsque le document est signé, car il doit être fourni par le serveur de certificats de l’ordinateur client lorsque la signature est validée.


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
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

[Vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**Utilisé dans cet exemple**
</dt> <dt>

[**contexte du certificat \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**\_informations d’OID de chiffre \_**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**IOpcCertificateSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[API de chiffrement](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Fonctions de chiffrement](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Certificats numériques](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Chaînes de certificats](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Vérification de l’approbation du certificat](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[Erreurs de l’API de signature numérique XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erreurs de document XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
