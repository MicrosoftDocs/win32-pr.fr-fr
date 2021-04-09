---
description: Cette rubrique décrit comment signer un document XPS.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Signer un document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864746"
---
# <a name="sign-a-document"></a><span data-ttu-id="66d10-103">Signer un document</span><span class="sxs-lookup"><span data-stu-id="66d10-103">Sign a Document</span></span>

<span data-ttu-id="66d10-104">Cette rubrique décrit comment signer un document XPS.</span><span class="sxs-lookup"><span data-stu-id="66d10-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="66d10-105">Avant d’utiliser les exemples de code suivants dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de signature numérique courantes](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="66d10-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="66d10-106">Pour signer un document XPS, commencez par le charger dans un gestionnaire de signature, comme décrit dans [initialiser le gestionnaire de signatures](initialize-the-signature-manager.md).</span><span class="sxs-lookup"><span data-stu-id="66d10-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="66d10-107">Pour signer un document qui a été chargé dans un gestionnaire de signature :</span><span class="sxs-lookup"><span data-stu-id="66d10-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="66d10-108">Instanciez une interface [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) .</span><span class="sxs-lookup"><span data-stu-id="66d10-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="66d10-109">Définissez la stratégie de signature.</span><span class="sxs-lookup"><span data-stu-id="66d10-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="66d10-110">Définissez la méthode de signature.</span><span class="sxs-lookup"><span data-stu-id="66d10-110">Set the signature method.</span></span> <span data-ttu-id="66d10-111">Les constantes de chaîne d’URI de méthode de signature sont définies dans cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="66d10-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="66d10-112">Pour plus d’informations sur les valeurs de méthode de signature valides, consultez [**IXpsSigningOptions :: SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span><span class="sxs-lookup"><span data-stu-id="66d10-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="66d10-113">Définissez la méthode Digest.</span><span class="sxs-lookup"><span data-stu-id="66d10-113">Set the digest method.</span></span> <span data-ttu-id="66d10-114">Les constantes de chaîne d’URI de méthode Digest sont définies dans cryptxml. h.</span><span class="sxs-lookup"><span data-stu-id="66d10-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="66d10-115">Pour plus d’informations sur les valeurs de méthode Digest valides, consultez [**IXpsSigningOptions :: SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span><span class="sxs-lookup"><span data-stu-id="66d10-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="66d10-116">Chargez le certificat comme décrit dans [charger un certificat à partir d’un fichier](load-a-certificate-from-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="66d10-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="66d10-117">Vérifiez que le certificat prend en charge la méthode de signature, comme décrit dans [vérifier qu’un certificat prend en charge une méthode de signature](verify-a-certificate-supports-a-signature-method.md).</span><span class="sxs-lookup"><span data-stu-id="66d10-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="66d10-118">Vérifiez que la méthode Digest est prise en charge par le système, comme décrit dans [vérifier que le système prend en charge une méthode Digest](verify-a-certificate-supports-a-digest-method.md).</span><span class="sxs-lookup"><span data-stu-id="66d10-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="66d10-119">Si nécessaire, incorporez les certificats de la chaîne d’approbation de certificat dans le document XPS comme décrit dans [incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="66d10-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="66d10-120">Signez le document XPS.</span><span class="sxs-lookup"><span data-stu-id="66d10-120">Sign the XPS document.</span></span>

<span data-ttu-id="66d10-121">L’exemple de code suivant illustre l’utilisation des étapes précédentes dans un programme.</span><span class="sxs-lookup"><span data-stu-id="66d10-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="66d10-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66d10-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="66d10-123">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="66d10-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="66d10-124">Ajouter une demande de signature à un document XPS</span><span class="sxs-lookup"><span data-stu-id="66d10-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="66d10-125">Vérifier les signatures de document</span><span class="sxs-lookup"><span data-stu-id="66d10-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="66d10-126">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="66d10-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="66d10-127">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="66d10-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="66d10-128">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="66d10-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="66d10-129">**IXpsSignatureManager::CreateSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="66d10-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="66d10-130">**IXpsSignatureManager :: Sign**</span><span class="sxs-lookup"><span data-stu-id="66d10-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="66d10-131">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="66d10-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="66d10-132">**IXpsSigningOptions::SetDigestMethod**</span><span class="sxs-lookup"><span data-stu-id="66d10-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="66d10-133">**IXpsSigningOptions::SetPolicy**</span><span class="sxs-lookup"><span data-stu-id="66d10-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="66d10-134">**IXpsSigningOptions::SetSignatureMethod**</span><span class="sxs-lookup"><span data-stu-id="66d10-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="66d10-135">**\_stratégie de signature XPS \_**</span><span class="sxs-lookup"><span data-stu-id="66d10-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="66d10-136">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="66d10-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="66d10-137">API de chiffrement</span><span class="sxs-lookup"><span data-stu-id="66d10-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="66d10-138">Fonctions de chiffrement</span><span class="sxs-lookup"><span data-stu-id="66d10-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="66d10-139">Charger un certificat à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="66d10-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="66d10-140">Vérifier qu’un certificat prend en charge une méthode de signature</span><span class="sxs-lookup"><span data-stu-id="66d10-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="66d10-141">Vérifier que le système prend en charge une méthode Digest</span><span class="sxs-lookup"><span data-stu-id="66d10-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="66d10-142">Incorporer des chaînes de certificats dans un document</span><span class="sxs-lookup"><span data-stu-id="66d10-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="66d10-143">Erreurs de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="66d10-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="66d10-144">Erreurs de document XPS</span><span class="sxs-lookup"><span data-stu-id="66d10-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="66d10-145">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="66d10-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
