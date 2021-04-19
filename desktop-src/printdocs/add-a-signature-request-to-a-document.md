---
description: Cette rubrique explique comment ajouter une demande de signature à un document XPS.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Ajouter une demande de signature à un document XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545030"
---
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="c7d66-103">Ajouter une demande de signature à un document XPS</span><span class="sxs-lookup"><span data-stu-id="c7d66-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="c7d66-104">Cette rubrique explique comment ajouter une demande de signature à un document XPS.</span><span class="sxs-lookup"><span data-stu-id="c7d66-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="c7d66-105">Une demande de signature invite un utilisateur à signer un document s’il accepte l’intention de signature.</span><span class="sxs-lookup"><span data-stu-id="c7d66-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="c7d66-106">Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c7d66-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="c7d66-107">Pour ajouter une demande de signature à un document XPS :</span><span class="sxs-lookup"><span data-stu-id="c7d66-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="c7d66-108">Chargez le document XPS dans un gestionnaire de signature, comme décrit dans [initialiser le gestionnaire de signatures](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="c7d66-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="c7d66-109">Ajoutez un bloc de signature au gestionnaire de signatures.</span><span class="sxs-lookup"><span data-stu-id="c7d66-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="c7d66-110">Créez une demande de signature dans le nouveau bloc de signature.</span><span class="sxs-lookup"><span data-stu-id="c7d66-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="c7d66-111">Définissez les propriétés de la demande de signature :</span><span class="sxs-lookup"><span data-stu-id="c7d66-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="c7d66-112">Définissez l’intention de signature.</span><span class="sxs-lookup"><span data-stu-id="c7d66-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="c7d66-113">Définissez le nom de la personne dont la signature est demandée (le signataire demandé).</span><span class="sxs-lookup"><span data-stu-id="c7d66-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="c7d66-114">Définissez la date à laquelle la signature est requise.</span><span class="sxs-lookup"><span data-stu-id="c7d66-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="c7d66-115">Définissez d’autres propriétés de signature selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c7d66-115">Set other signature properties as required.</span></span>

<span data-ttu-id="c7d66-116">L’exemple de code suivant montre comment ajouter une demande de signature à un document XPS.</span><span class="sxs-lookup"><span data-stu-id="c7d66-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c7d66-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7d66-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c7d66-118">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="c7d66-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="c7d66-119">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="c7d66-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="c7d66-120">**IXpsSignatureBlock::CreateRequest**</span><span class="sxs-lookup"><span data-stu-id="c7d66-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="c7d66-121">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="c7d66-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="c7d66-122">**IXpsSignatureManager::AddSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="c7d66-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="c7d66-123">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="c7d66-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="c7d66-124">**IXpsSignatureRequest::SetIntent**</span><span class="sxs-lookup"><span data-stu-id="c7d66-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="c7d66-125">**IXpsSignatureRequest::SetRequestedSigner**</span><span class="sxs-lookup"><span data-stu-id="c7d66-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="c7d66-126">**IXpsSignatureRequest::SetRequestSignByDate**</span><span class="sxs-lookup"><span data-stu-id="c7d66-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="c7d66-127">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="c7d66-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="c7d66-128">Erreurs de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="c7d66-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="c7d66-129">Erreurs de document XPS</span><span class="sxs-lookup"><span data-stu-id="c7d66-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="c7d66-130">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="c7d66-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



