---
description: Crée un objet de demande CMC à partir d’une requête PKCS 10 imbriquée interne \# .
ms.assetid: 8a0dc078-22ca-4bff-9cc0-46823912d3da
title: createCNGCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669a52901981ea910ee3d1704ba892fb96664470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318069"
---
# <a name="createcngcustomcmc"></a><span data-ttu-id="6ae8b-103">createCNGCustomCMC</span><span class="sxs-lookup"><span data-stu-id="6ae8b-103">createCNGCustomCMC</span></span>

<span data-ttu-id="6ae8b-104">L’exemple createCNGCustomCMC crée un objet de demande CMC à partir d’une requête PKCS 10 imbriquée interne \# .</span><span class="sxs-lookup"><span data-stu-id="6ae8b-104">The createCNGCustomCMC sample creates a CMC request object from an inner nested PKCS \#10 request.</span></span> <span data-ttu-id="6ae8b-105">La requête interne est créée à l’aide d’une [*clé privée*](/windows/desktop/SecGloss/p-gly)asymétrique.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-105">The inner request is created by using an asymmetric [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="6ae8b-106">La clé privée est créée à l’aide du fournisseur de services de chiffrement Cryptography API : Next Generation (CNG) et de l’algorithme spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-106">The private key is created by using the Cryptography API: Next Generation (CNG) cryptographic provider and the algorithm specified on the command line.</span></span> <span data-ttu-id="6ae8b-107">Les options personnalisées, telles que la stratégie d’exportation et le niveau de protection de clé, sont également définies sur la clé privée.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-107">Custom options such as export policy and key protection level are also set on the private key.</span></span>

## <a name="location"></a><span data-ttu-id="6ae8b-108">Emplacement</span><span class="sxs-lookup"><span data-stu-id="6ae8b-108">Location</span></span>

<span data-ttu-id="6ae8b-109">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ createCNGCustomCMC VC.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-109">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\createCNGCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="6ae8b-110">Discussions</span><span class="sxs-lookup"><span data-stu-id="6ae8b-110">Discussion</span></span>

<span data-ttu-id="6ae8b-111">Exemple createCNGCustomCMC :</span><span class="sxs-lookup"><span data-stu-id="6ae8b-111">The createCNGCustomCMC sample:</span></span>

1.  <span data-ttu-id="6ae8b-112">Traite les arguments de ligne de commande suivants :</span><span class="sxs-lookup"><span data-stu-id="6ae8b-112">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="6ae8b-113">Nom d’un fournisseur de [*services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) CNG.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-113">The name of a CNG [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span>
    -   <span data-ttu-id="6ae8b-114">Nom de l’algorithme utilisé pour générer une clé privée asymétrique.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-114">The name of the algorithm used to generate an asymmetric private key.</span></span>
    -   <span data-ttu-id="6ae8b-115">Nom de l’algorithme utilisé pour [*hacher*](/windows/desktop/SecGloss/h-gly) la [*demande de certificat*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="6ae8b-115">The name of the algorithm used to [*hash*](/windows/desktop/SecGloss/h-gly) the [*certificate request*](/windows/desktop/SecGloss/c-gly).</span></span>
    -   <span data-ttu-id="6ae8b-116">Fichier de sortie dans lequel enregistrer la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-116">An output file in which to save the certificate request.</span></span>
    -   <span data-ttu-id="6ae8b-117">Chaîne facultative (AlternateSignature) qui, si elle est présente, spécifie qu’un algorithme discret plutôt qu’un algorithme de signature combiné doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-117">An optional string (AlternateSignature) which, if present, specifies that a discrete rather than a combined signature algorithm be used.</span></span> <span data-ttu-id="6ae8b-118">Pour plus d’informations, consultez la propriété [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) .</span><span class="sxs-lookup"><span data-stu-id="6ae8b-118">For more information, see the [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm) property.</span></span>
2.  <span data-ttu-id="6ae8b-119">Crée un objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) et définit les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ae8b-119">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object and sets the following properties:</span></span>
    -   [<span data-ttu-id="6ae8b-120">**LegacyCsp**</span><span class="sxs-lookup"><span data-stu-id="6ae8b-120">**LegacyCsp**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_legacycsp)
    -   [<span data-ttu-id="6ae8b-121">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="6ae8b-121">**ProviderName**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername)
    -   [<span data-ttu-id="6ae8b-122">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="6ae8b-122">**Algorithm**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm)
    -   [<span data-ttu-id="6ae8b-123">**Keyprotection**</span><span class="sxs-lookup"><span data-stu-id="6ae8b-123">**KeyProtection**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyprotection)
    -   [<span data-ttu-id="6ae8b-124">**ExportPolicy**</span><span class="sxs-lookup"><span data-stu-id="6ae8b-124">**ExportPolicy**</span></span>](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_exportpolicy)
3.  <span data-ttu-id="6ae8b-125">Crée une clé privée asymétrique.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-125">Creates an asymmetric private key.</span></span>
4.  <span data-ttu-id="6ae8b-126">Crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise à l’aide de la clé privée.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-126">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the private key.</span></span>
5.  <span data-ttu-id="6ae8b-127">Crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise à l’aide de l' \# objet de requête PKCS 10 créé à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-127">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object created in step 4.</span></span>
6.  <span data-ttu-id="6ae8b-128">Définit l’indicateur de l’algorithme de signature alternatif sur **Variant \_ true** ou **\_ false variant** selon qu’une autre chaîne de signature est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-128">Sets the alternate signature algorithm flag to **VARIANT\_TRUE** or **VARIANT\_FALSE** depending on whether an alternate signature string is specified on the command line.</span></span> <span data-ttu-id="6ae8b-129">Pour plus d’informations, consultez [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span><span class="sxs-lookup"><span data-stu-id="6ae8b-129">For more information, see [**AlternateSignatureAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-get_alternatesignaturealgorithm).</span></span>
7.  <span data-ttu-id="6ae8b-130">Crée un [*identificateur d’objet*](/windows/desktop/SecGloss/o-gly) (OID) d' [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) à partir du nom de l’algorithme spécifié sur la ligne de commande et définit l’OID sur l’objet de demande CMC.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-130">Creates a [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) from the algorithm name specified on the command line and sets the OID on the CMC request object.</span></span>
8.  <span data-ttu-id="6ae8b-131">Signe la demande de certificat et l’encode à l’aide d' [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="6ae8b-131">Signs the certificate request and encodes it by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
9.  <span data-ttu-id="6ae8b-132">Récupère une chaîne qui contient la demande de certificat CMC encodée et l’enregistre dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-132">Retrieves a string that contains the encoded CMC certificate request and saves it to a file.</span></span> <span data-ttu-id="6ae8b-133">La fonction EncodeToFileW est définie dans EnrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="6ae8b-133">The EncodeToFileW function is defined in EnrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ae8b-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ae8b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ae8b-135">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="6ae8b-135">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="6ae8b-136">\#Demande PKCS 10</span><span class="sxs-lookup"><span data-stu-id="6ae8b-136">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="6ae8b-137">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="6ae8b-137">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> <dt>

[<span data-ttu-id="6ae8b-138">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="6ae8b-138">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
