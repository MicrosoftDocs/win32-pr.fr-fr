---
description: Cette rubrique répertorie les considérations relatives à l’utilisation de l’API de signature numérique XPS pour ajouter des signatures numériques à un document XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Utilisation de l’API de signature numérique XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864954"
---
# <a name="using-xps-digital-signature-api"></a><span data-ttu-id="9c418-103">Utilisation de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-103">Using XPS Digital Signature API</span></span>

<span data-ttu-id="9c418-104">Cette rubrique répertorie les considérations relatives à l’utilisation de l’API de signature numérique XPS pour ajouter des signatures numériques à un document XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-104">This topic lists considerations for using the XPS Digital Signature API to add digital signatures to an XPS document.</span></span>

<span data-ttu-id="9c418-105">L’API de signature numérique XPS permet aux applications de demander aux utilisateurs de signer des documents XPS et de vérifier les signatures détectées dans les documents XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-105">The XPS Digital Signature API enables applications to request users to sign XPS documents and to verify signatures that are found in XPS documents.</span></span> <span data-ttu-id="9c418-106">L’API de signature numérique XPS peut être appliquée à un document XPS sans le charger dans un modèle d’objet XPS, et elle peut être utilisée sur les flux de documents XPS qui sont sérialisés à partir d’un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-106">The XPS Digital Signature API can be applied to an XPS document without loading it into an XPS OM, and it can be used on XPS document streams that are serialized from an XPS OM.</span></span>

<span data-ttu-id="9c418-107">La section des tâches de programmation de l' [API de signature numérique XPS](#xps-digital-signature-api-programming-tasks) contient des rubriques qui décrivent comment programmer avec l’API de signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-107">The [XPS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) section contains topics that describe how to program with the XPS Digital Signature API.</span></span> <span data-ttu-id="9c418-108">Cette rubrique présente les éléments à prendre en considération pour l’utilisation de l’API de signature numérique XPS lors de l’ajout de la prise en charge des signatures numériques à une application.</span><span class="sxs-lookup"><span data-stu-id="9c418-108">This topic lists the following considerations for using the XPS Digital Signature API when adding digital signature support to an application.</span></span>

-   [<span data-ttu-id="9c418-109">Tâches de programmation de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-109">XPS Digital Signature API Programming Tasks</span></span>](#xps-digital-signature-api-programming-tasks)
-   [<span data-ttu-id="9c418-110">Remarques spéciales sur la programmation de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-110">Special Notes about XPS Digital Signature API Programming</span></span>](#special-notes-about-xps-digital-signature-api-programming)
    -   [<span data-ttu-id="9c418-111">Vérification des signatures numériques dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-111">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
    -   [<span data-ttu-id="9c418-112">Stratégie de signature des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="9c418-112">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
    -   [<span data-ttu-id="9c418-113">Incorporation d’une chaîne de certificats</span><span class="sxs-lookup"><span data-stu-id="9c418-113">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
    -   [<span data-ttu-id="9c418-114">Utilisation de la \_ structure de contexte du certificat</span><span class="sxs-lookup"><span data-stu-id="9c418-114">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)
-   [<span data-ttu-id="9c418-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c418-115">Related topics</span></span>](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a><span data-ttu-id="9c418-116">Tâches de programmation de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-116">XPS Digital Signature API Programming Tasks</span></span>

<span data-ttu-id="9c418-117">Cette section contient des rubriques qui décrivent comment effectuer des tâches de programmation à l’aide de l’API de signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-117">This section contains topics that describe how to perform programming tasks by using the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="9c418-118">Tâches courantes de programmation des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="9c418-118">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="9c418-119">Initialiser le gestionnaire de signatures</span><span class="sxs-lookup"><span data-stu-id="9c418-119">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)  
    [<span data-ttu-id="9c418-120">Signer un document</span><span class="sxs-lookup"><span data-stu-id="9c418-120">Sign a Document</span></span>](sign-a-document.md)  
    [<span data-ttu-id="9c418-121">Ajouter une demande de signature à un document XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-121">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)  
    [<span data-ttu-id="9c418-122">Vérifier les signatures de document</span><span class="sxs-lookup"><span data-stu-id="9c418-122">Verify Document Signatures</span></span>](verify-document-signatures.md)  
    </dl>
-   [<span data-ttu-id="9c418-123">Tâches de programmation de signature numérique supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9c418-123">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)<dl>

[<span data-ttu-id="9c418-124">Charger un certificat à partir d’un fichier</span><span class="sxs-lookup"><span data-stu-id="9c418-124">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)  
    [<span data-ttu-id="9c418-125">Vérifier qu’un certificat prend en charge une méthode de signature</span><span class="sxs-lookup"><span data-stu-id="9c418-125">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)  
    [<span data-ttu-id="9c418-126">Vérifier que le système prend en charge une méthode Digest</span><span class="sxs-lookup"><span data-stu-id="9c418-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)  
    [<span data-ttu-id="9c418-127">Incorporer des chaînes de certificats dans un document</span><span class="sxs-lookup"><span data-stu-id="9c418-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a><span data-ttu-id="9c418-128">Remarques spéciales sur la programmation de l’API de signature numérique XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-128">Special Notes about XPS Digital Signature API Programming</span></span>

<span data-ttu-id="9c418-129">Les rubriques suivantes nécessitent une attention particulière lorsque vous utilisez l’API de signature numérique XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-129">The following topics require some special consideration when you use the XPS Digital Signature API.</span></span>

-   [<span data-ttu-id="9c418-130">Vérification des signatures numériques dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-130">Verifying Digital Signatures in an XPS Document</span></span>](#verifying-digital-signatures-in-an-xps-document)
-   [<span data-ttu-id="9c418-131">Stratégie de signature des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="9c418-131">Digital Signature Signing Policy</span></span>](#digital-signature-signing-policy)
-   [<span data-ttu-id="9c418-132">Incorporation d’une chaîne de certificats</span><span class="sxs-lookup"><span data-stu-id="9c418-132">Embedding a Certificate Chain</span></span>](#embedding-a-certificate-chain)
-   [<span data-ttu-id="9c418-133">Utilisation de la \_ structure de contexte du certificat</span><span class="sxs-lookup"><span data-stu-id="9c418-133">Using the CERT\_CONTEXT Structure</span></span>](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a><span data-ttu-id="9c418-134">Vérification des signatures numériques dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="9c418-134">Verifying Digital Signatures in an XPS Document</span></span>

<span data-ttu-id="9c418-135">[**IXpsSignature :: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) vérifie uniquement le contenu signé pour déterminer qu’il n’a pas été modifié depuis sa signature.</span><span class="sxs-lookup"><span data-stu-id="9c418-135">[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) checks only the signed content to determine that it has not changed since it was signed.</span></span> <span data-ttu-id="9c418-136">**IXpsSignature :: Verify** ne vérifie pas les certificats qui ont été utilisés pour signer le contenu du document.</span><span class="sxs-lookup"><span data-stu-id="9c418-136">**IXpsSignature::Verify** does not verify any of the certificates that were used to sign the document content.</span></span>

<span data-ttu-id="9c418-137">Pour plus d’informations sur les certificats et le chiffrement, consultez [à propos du chiffrement](/windows/desktop/SecCrypto/about-cryptography).</span><span class="sxs-lookup"><span data-stu-id="9c418-137">For more information about certificates and cryptography, see [About Cryptography](/windows/desktop/SecCrypto/about-cryptography).</span></span>

<span data-ttu-id="9c418-138">Pour obtenir un exemple de vérification des signatures de document dans un programme, consultez [vérifier les signatures de documents et les certificats](verify-document-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="9c418-138">For an example of how to verify document signatures in a program, see [Verify Document Signatures and Certificates](verify-document-signatures.md).</span></span>

### <a name="digital-signature-signing-policy"></a><span data-ttu-id="9c418-139">Stratégie de signature des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="9c418-139">Digital Signature Signing Policy</span></span>

<span data-ttu-id="9c418-140">La stratégie de signature de signature numérique détermine les parties d’un document XPS signées.</span><span class="sxs-lookup"><span data-stu-id="9c418-140">The digital signature signing policy determines which parts of an XPS document are signed.</span></span> <span data-ttu-id="9c418-141">Une option de stratégie de signature consiste à signer les relations de signature qui démarrent à partir de la partie origine de la signature.</span><span class="sxs-lookup"><span data-stu-id="9c418-141">One signing policy option is to sign the signature relationships that start from the signature origin part.</span></span> <span data-ttu-id="9c418-142">Étant donné que les relations de signature changent avec chaque signature ajoutée, les signatures qui sont effectuées dans le cadre de cette stratégie s’interrompent lors de l’ajout de nouvelles signatures.</span><span class="sxs-lookup"><span data-stu-id="9c418-142">Because the signature relationships change with each signature that is added, signatures that are made under this policy will break when new signatures are added.</span></span> <span data-ttu-id="9c418-143">Assurez-vous que vous comprenez clairement les implications et les effets de la définition de cette stratégie. dans le cas contraire, un comportement inattendu ou indésirable peut se produire.</span><span class="sxs-lookup"><span data-stu-id="9c418-143">Make sure that you understand clearly the implications and effects of setting this policy; otherwise, unexpected or undesired behavior might result.</span></span>

<span data-ttu-id="9c418-144">Pour plus d’informations sur les stratégies de signature, consultez [**\_ \_ stratégie**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)de signature XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-144">For more information about signing policies, see [**XPS\_SIGN\_POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).</span></span>

### <a name="embedding-a-certificate-chain"></a><span data-ttu-id="9c418-145">Incorporation d’une chaîne de certificats</span><span class="sxs-lookup"><span data-stu-id="9c418-145">Embedding a Certificate Chain</span></span>

<span data-ttu-id="9c418-146">Les certificats qui composent la chaîne d’approbation d’un certificat spécifique peuvent être ajoutés à un document XPS.</span><span class="sxs-lookup"><span data-stu-id="9c418-146">The certificates that make up the trust chain of a specific certificate can be added to an XPS document.</span></span> <span data-ttu-id="9c418-147">L’incorporation de ces certificats peut faciliter, dans des scénarios hors ligne, qu’une application vérifie les certificats qu’une signature numérique utilise.</span><span class="sxs-lookup"><span data-stu-id="9c418-147">Embedding these certificates can make it easier, in off-line scenarios, for an application to verify the certificates that a digital signature uses.</span></span>

<span data-ttu-id="9c418-148">Pour plus d’informations sur la façon d’incorporer des certificats dans un document XPS, consultez [incorporer des chaînes de certificats dans un document](embedding-certificate-trust-chains-in-a-document.md).</span><span class="sxs-lookup"><span data-stu-id="9c418-148">For more information about how to embed certificates in an XPS document, see [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>

### <a name="using-the-cert_context-structure"></a><span data-ttu-id="9c418-149">Utilisation de la \_ structure de contexte du certificat</span><span class="sxs-lookup"><span data-stu-id="9c418-149">Using the CERT\_CONTEXT Structure</span></span>

<span data-ttu-id="9c418-150">Le [**\_ contexte**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificat et les structures d' [**\_ informations**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) de certificat sont les structures de données principales qui contiennent les informations de certificat.</span><span class="sxs-lookup"><span data-stu-id="9c418-150">The [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) and [**CERT\_INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) structures are the main data structures that hold certificate information.</span></span> <span data-ttu-id="9c418-151">Pour plus d’informations sur l’utilisation de ces structures, consultez [utilisation d’une \_ structure de données d’informations de certificat](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span><span class="sxs-lookup"><span data-stu-id="9c418-151">For more information about using these structures, see [Using a CERT\_INFO Data Structure](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).</span></span>

<span data-ttu-id="9c418-152">[**Certificat \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Les structures de contexte retournées par les fonctions API de chiffrement doivent être libérées lorsqu’elles ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9c418-152">[**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures that are returned by Crypto API functions must be released when they are no longer needed.</span></span> <span data-ttu-id="9c418-153">Pour libérer une structure de **\_ contexte de certificat** , appelez la fonction [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="9c418-153">To release a **CERT\_CONTEXT** structure, call the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c418-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c418-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c418-155">Tâches courantes de programmation des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="9c418-155">Common Digital Signature Programming Tasks</span></span>](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="9c418-156">Tâches de programmation de signature numérique supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9c418-156">Additional Digital Signature Programming Tasks</span></span>](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[<span data-ttu-id="9c418-157">**contexte du certificat \_**</span><span class="sxs-lookup"><span data-stu-id="9c418-157">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="9c418-158">**\_informations sur le certificat**</span><span class="sxs-lookup"><span data-stu-id="9c418-158">**CERT\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[<span data-ttu-id="9c418-159">**CertFreeCertificateContext**</span><span class="sxs-lookup"><span data-stu-id="9c418-159">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="9c418-160">**\_stratégie de signature XPS \_**</span><span class="sxs-lookup"><span data-stu-id="9c418-160">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[<span data-ttu-id="9c418-161">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="9c418-161">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
