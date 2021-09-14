---
description: Cette rubrique explique comment ajouter une demande de signature à un document XPS.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Ajouter une demande de signature à un document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231666"
---
# <a name="add-a-signature-request-to-an-xps-document"></a>Ajouter une demande de signature à un document XPS

Cette rubrique explique comment ajouter une demande de signature à un document XPS. Une demande de signature invite un utilisateur à signer un document s’il accepte l’intention de signature.

Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).

Pour ajouter une demande de signature à un document XPS :

1.  Chargez le document XPS dans un gestionnaire de signature, comme décrit dans [initialiser le gestionnaire de signatures](initialize-the-signature-manager.md).
2.  Ajoutez un bloc de signature au gestionnaire de signatures.
3.  Créez une demande de signature dans le nouveau bloc de signature.
4.  Définissez les propriétés de la demande de signature :
    1.  Définissez l’intention de signature.
    2.  Définissez le nom de la personne dont la signature est demandée (le signataire demandé).
    3.  Définissez la date à laquelle la signature est requise.
    4.  Définissez d’autres propriétés de signature selon vos besoins.

L’exemple de code suivant montre comment ajouter une demande de signature à un document XPS.


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Utilisé dans cette section**
</dt> <dt>

[**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[**IXpsSignatureBlock::CreateRequest**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::AddSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[**IXpsSignatureRequest::SetIntent**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[**IXpsSignatureRequest::SetRequestedSigner**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[**IXpsSignatureRequest::SetRequestSignByDate**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

**Pour plus d’informations**
</dt> <dt>

[Erreurs de l’API de signature numérique XPS](xps-digital-signatures-errors.md)
</dt> <dt>

[Erreurs de document XPS](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



