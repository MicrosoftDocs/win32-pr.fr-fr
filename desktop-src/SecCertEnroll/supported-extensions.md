---
description: Vous pouvez utiliser l’interface IX509Extension pour définir une extension arbitraire.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensions prises en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752164"
---
# <a name="supported-extensions"></a><span data-ttu-id="7690c-103">Extensions prises en charge</span><span class="sxs-lookup"><span data-stu-id="7690c-103">Supported Extensions</span></span>

<span data-ttu-id="7690c-104">Vous pouvez utiliser l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) pour définir une extension arbitraire.</span><span class="sxs-lookup"><span data-stu-id="7690c-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="7690c-105">L’API d’inscription de certificats fournit également des interfaces dérivées de **IX509Extension** pour vous permettre de créer facilement les extensions les plus courantes.</span><span class="sxs-lookup"><span data-stu-id="7690c-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="7690c-106">La liste suivante identifie les extensions communes prises en charge par les autorités de certification Microsoft, ainsi que les identificateurs d’objets et les interfaces que vous pouvez utiliser pour les créer.</span><span class="sxs-lookup"><span data-stu-id="7690c-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="7690c-107">AlternativeNames</span><span class="sxs-lookup"><span data-stu-id="7690c-107">AlternativeNames</span></span>

<span data-ttu-id="7690c-108">L’extension de noms alternatifs peut être utilisée pour définir une ou plusieurs autres formes de nom pour l’objet de la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="7690c-109">Parmi les autres formes, citons : adresses de messagerie, noms DNS, adresses IP et URI.</span><span class="sxs-lookup"><span data-stu-id="7690c-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="7690c-110">**Interface :** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="7690c-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="7690c-111">**OID :** XCN \_ OID \_ Subject \_ Alt \_ nom2 (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="7690c-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="7690c-112">AuthorityInformationAccess</span><span class="sxs-lookup"><span data-stu-id="7690c-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="7690c-113">L’extension d’accès aux informations de l’autorité identifie l’accès aux informations et aux services de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="7690c-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="7690c-114">La valeur d’extension contient une séquence d’URI.</span><span class="sxs-lookup"><span data-stu-id="7690c-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="7690c-115">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-116">**OID :** XCN \_ OID \_ Authority \_ info \_ Access (1.3.6.1.5.5.7.1.1)</span><span class="sxs-lookup"><span data-stu-id="7690c-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="7690c-117">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="7690c-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="7690c-118">L’extension de l’identificateur de clé de l’autorité permet l’identification de la clé publique de l’autorité de certification qui correspond à la clé privée de l’autorité de certification qui a signé un certificat émis.</span><span class="sxs-lookup"><span data-stu-id="7690c-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="7690c-119">Il est utilisé par le logiciel de création de chemin d’accès de certificat sur un serveur Windows pour rechercher le certificat d’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="7690c-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="7690c-120">Lorsqu’une autorité de certification émet un certificat, la valeur de l’extension est égale à l’extension **extension SubjectKeyIdentifier** dans le certificat de signature de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="7690c-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="7690c-121">La valeur est généralement un hachage SHA-1 de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="7690c-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="7690c-122">**Interface :** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="7690c-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="7690c-123">**OID :** \_ \_ Clé de l’autorité XCN OID \_ \_ identificateur2 (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="7690c-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="7690c-124">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="7690c-124">BasicConstraints</span></span>

<span data-ttu-id="7690c-125">L’extension de contraintes de base peut être utilisée pour déterminer si l’entité peut être utilisée en tant qu’autorité de certification (CA) et, le cas échéant, le nombre d’autorités de certification secondaires qui peuvent exister sous celle-ci dans la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="7690c-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="7690c-126">**Interface :** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="7690c-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="7690c-127">**OID :** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="7690c-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="7690c-128">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="7690c-128">CertificatePolicies</span></span>

<span data-ttu-id="7690c-129">L’extension des stratégies de certificat peut être utilisée pour identifier les stratégies sous lesquelles le certificat a été émis, ainsi que les objectifs qui peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="7690c-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="7690c-130">Celles-ci sont identifiées par une collection d’identificateurs d’objet (OID).</span><span class="sxs-lookup"><span data-stu-id="7690c-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="7690c-131">Les stratégies sont personnalisées pour les besoins d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="7690c-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="7690c-132">**Interface :** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="7690c-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="7690c-133">**OID :** \_ \_ Stratégies de certificat XCN OID \_ (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="7690c-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="7690c-134">CrlDistributionPoints</span><span class="sxs-lookup"><span data-stu-id="7690c-134">CrlDistributionPoints</span></span>

<span data-ttu-id="7690c-135">L’extension des points de distribution de la liste de révocation de certificats (CRL) contient l’URI de la liste de révocation de certificats de base.</span><span class="sxs-lookup"><span data-stu-id="7690c-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="7690c-136">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-137">**OID :** \_ \_ Points de distribution de liste de révocation de certificats XCN OID \_ \_ (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="7690c-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="7690c-138">Champ EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="7690c-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="7690c-139">L’extension utilisation améliorée de la clé peut être utilisée pour définir une ou plusieurs utilisations de la clé publique contenue dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="7690c-140">**Interface :** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="7690c-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="7690c-141">**OID :** \_ \_ Utilisation améliorée de la clé XCN OID \_ \_ (2.5.29.37)</span><span class="sxs-lookup"><span data-stu-id="7690c-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="7690c-142">FreshestCRL</span><span class="sxs-lookup"><span data-stu-id="7690c-142">FreshestCRL</span></span>

<span data-ttu-id="7690c-143">L’extension de la liste de révocation de certificats la plus récente contient l’URI de la liste CRL Delta.</span><span class="sxs-lookup"><span data-stu-id="7690c-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="7690c-144">La même syntaxe ASN. 1 est utilisée pour cette extension et l’extension **CrlDistributionPoints** .</span><span class="sxs-lookup"><span data-stu-id="7690c-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="7690c-145">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-146">**OID :** XCN \_ OID le plus \_ actualisé \_ (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="7690c-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="7690c-147">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7690c-147">KeyUsage</span></span>

<span data-ttu-id="7690c-148">L’extension d’utilisation de la clé peut être utilisée pour définir des restrictions sur les opérations qui peuvent être effectuées par la clé publique contenue dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="7690c-149">Par exemple, vous pouvez spécifier que la clé publique doit être utilisée uniquement pour créer une signature numérique, signer une liste de révocation de certificats (CRL) ou chiffrer une autre clé.</span><span class="sxs-lookup"><span data-stu-id="7690c-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="7690c-150">**Interface :** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="7690c-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="7690c-151">**OID :** \_ \_ Utilisation de la clé XCN OID \_ (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="7690c-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="7690c-152">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="7690c-152">MSApplicationPolicies</span></span>

<span data-ttu-id="7690c-153">L’extension des stratégies d’application Microsoft peut être utilisée par une application pour filtrer les certificats sur la base de l’utilisation autorisée.</span><span class="sxs-lookup"><span data-stu-id="7690c-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="7690c-154">Les utilisations autorisées sont identifiées par des OID.</span><span class="sxs-lookup"><span data-stu-id="7690c-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="7690c-155">Cette extension est similaire à l’extension **champ EnhancedKeyUsage** , mais avec des sémantiques plus strictes appliquées à l’autorité de certification parente.</span><span class="sxs-lookup"><span data-stu-id="7690c-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="7690c-156">L’extension est spécifique à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7690c-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="7690c-157">**Interface :** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="7690c-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="7690c-158">**OID :** XCN \_ OID \_ application \_ CERT \_ Policies (1.3.6.1.4.1.311.21.10)</span><span class="sxs-lookup"><span data-stu-id="7690c-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="7690c-159">NameConstraints</span><span class="sxs-lookup"><span data-stu-id="7690c-159">NameConstraints</span></span>

<span data-ttu-id="7690c-160">L’extension de contraintes de nom est utilisée pour identifier l’espace de noms dans lequel tous les noms d’objet des certificats dans une hiérarchie de certificats doivent être localisés.</span><span class="sxs-lookup"><span data-stu-id="7690c-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="7690c-161">L’extension n’est utilisée que dans un certificat d’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="7690c-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="7690c-162">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-163">**OID :** \_ \_ Contraintes de nom XCN OID \_ (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="7690c-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="7690c-164">PolicyConstraints</span><span class="sxs-lookup"><span data-stu-id="7690c-164">PolicyConstraints</span></span>

<span data-ttu-id="7690c-165">L’extension de contraintes de stratégie est ajoutée aux certificats de l’autorité de certification pour limiter la validation du chemin d’accès en interdisant le mappage de la stratégie ou en exigeant que chaque certificat de la hiérarchie contienne un identificateur de stratégie acceptable.</span><span class="sxs-lookup"><span data-stu-id="7690c-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="7690c-166">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-167">**OID :** \_ \_ Contraintes de la stratégie OID XCN \_ (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="7690c-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="7690c-168">PolicyMappings</span><span class="sxs-lookup"><span data-stu-id="7690c-168">PolicyMappings</span></span>

<span data-ttu-id="7690c-169">L’extension mappages de stratégie permet d’identifier les stratégies d’une autorité de certification secondaire qui correspondent aux stratégies de l’autorité de certification émettrice.</span><span class="sxs-lookup"><span data-stu-id="7690c-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="7690c-170">La valeur d’extension contient une séquence d’autorités de certification émettrices et des mappages de stratégie d’autorité de certification subordonnée représentés par des identificateurs d’objets.</span><span class="sxs-lookup"><span data-stu-id="7690c-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="7690c-171">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-172">**OID :** \_ \_ Mappages de la stratégie OID XCN \_ (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="7690c-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="7690c-173">PrivateKeyUsagePeriod</span><span class="sxs-lookup"><span data-stu-id="7690c-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="7690c-174">L’extension de période d’utilisation de la clé privée est utilisée pour spécifier une période de validité différente pour la clé privée que pour le certificat auquel la clé est associée.</span><span class="sxs-lookup"><span data-stu-id="7690c-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="7690c-175">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-176">**OID :** \_Période d' \_ utilisation de XCN OID PRIVATEKEY \_ \_ (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="7690c-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="7690c-177">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="7690c-177">SmimeCapabilities</span></span>

<span data-ttu-id="7690c-178">L’extension des fonctionnalités S/MIME (Secure/Multipurpose Internet Mail Extensions) peut être utilisée pour signaler les fonctionnalités de déchiffrement d’un destinataire de courrier électronique à l’expéditeur du message électronique, afin que l’expéditeur puisse choisir l’algorithme de chiffrement le plus sécurisé pris en charge par les deux parties.</span><span class="sxs-lookup"><span data-stu-id="7690c-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="7690c-179">La valeur d’extension contient une collection d’OID d’algorithme de chiffrement symétrique et une force de chiffrement facultative pour chacun.</span><span class="sxs-lookup"><span data-stu-id="7690c-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="7690c-180">**Interface :** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="7690c-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="7690c-181">**OID :** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)</span><span class="sxs-lookup"><span data-stu-id="7690c-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="7690c-182">SubjectDirectoryAttributes</span><span class="sxs-lookup"><span data-stu-id="7690c-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="7690c-183">L’extension des attributs du répertoire du sujet peut être utilisée pour transmettre des attributs d’identification tels que la nationalité de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="7690c-184">La valeur de l’extension est une séquence de paires OID-valeur.</span><span class="sxs-lookup"><span data-stu-id="7690c-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="7690c-185">**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="7690c-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="7690c-186">**OID :** XCN \_ OID \_ Subject \_ dir \_ ATTRS (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="7690c-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="7690c-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="7690c-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="7690c-188">L’extension de l’identificateur de clé du sujet peut être utilisée pour différencier plusieurs clés publiques détenues par l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="7690c-189">La valeur de l’extension est généralement un hachage SHA-1 de la clé.</span><span class="sxs-lookup"><span data-stu-id="7690c-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="7690c-190">**Interface :** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="7690c-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="7690c-191">**OID :** \_ \_ Identificateur de clé du sujet de l’OID XCN \_ \_ (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="7690c-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="7690c-192">Modèle</span><span class="sxs-lookup"><span data-stu-id="7690c-192">Template</span></span>

<span data-ttu-id="7690c-193">L’extension de modèle peut être utilisée pour identifier le modèle de version 2 à utiliser lors de l’émission ou du renouvellement d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="7690c-194">La valeur de l’extension contient l’OID du modèle et les informations de version facultatives.</span><span class="sxs-lookup"><span data-stu-id="7690c-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="7690c-195">L’extension est spécifique à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7690c-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="7690c-196">**Interface :** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="7690c-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="7690c-197">**OID :** \_ \_ Modèle de certificat XCN OID \_ (1.3.6.1.4.1.311.21.7)</span><span class="sxs-lookup"><span data-stu-id="7690c-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="7690c-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="7690c-198">TemplateName</span></span>

<span data-ttu-id="7690c-199">L’extension de nom de modèle peut être utilisée pour identifier le modèle de version 1 à utiliser lors de l’émission ou du renouvellement d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="7690c-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="7690c-200">La valeur de l’extension contient le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="7690c-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="7690c-201">L’extension est spécifique à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7690c-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="7690c-202">**Interface :** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="7690c-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="7690c-203">**OID :** XCN \_ OID \_ inscrire \_ le type \_ extension (1.3.6.1.4.1.311.20.2)</span><span class="sxs-lookup"><span data-stu-id="7690c-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7690c-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7690c-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7690c-205">Extensions</span><span class="sxs-lookup"><span data-stu-id="7690c-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



