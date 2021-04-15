---
description: Crée un \# objet de requête PKCS 7 pour renouveler un certificat existant. L’objet de requête utilise une nouvelle paire de clés, mais conserve le fournisseur de services de chiffrement associé au certificat en cours de renouvellement.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529391"
---
# <a name="enrollrenewalpkcs7"></a><span data-ttu-id="06a91-104">enrollRenewalPKCS7</span><span class="sxs-lookup"><span data-stu-id="06a91-104">enrollRenewalPKCS7</span></span>

<span data-ttu-id="06a91-105">L’exemple enrollRenewalPKCS7 crée un \# objet de demande PKCS 7 pour renouveler un certificat existant.</span><span class="sxs-lookup"><span data-stu-id="06a91-105">The enrollRenewalPKCS7 sample creates a PKCS \#7 request object to renew an existing certificate.</span></span> <span data-ttu-id="06a91-106">L’objet de requête utilise une nouvelle paire de clés, mais conserve le fournisseur de services de chiffrement associé au certificat en cours de renouvellement.</span><span class="sxs-lookup"><span data-stu-id="06a91-106">The request object uses a new key pair but retains the cryptographic provider associated with the certificate being renewed.</span></span>

## <a name="location"></a><span data-ttu-id="06a91-107">Emplacement</span><span class="sxs-lookup"><span data-stu-id="06a91-107">Location</span></span>

<span data-ttu-id="06a91-108">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollRenewalPKCS7 VC.</span><span class="sxs-lookup"><span data-stu-id="06a91-108">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollRenewalPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="06a91-109">Discussions</span><span class="sxs-lookup"><span data-stu-id="06a91-109">Discussion</span></span>

<span data-ttu-id="06a91-110">Exemple enrollRenewalPKCS7 :</span><span class="sxs-lookup"><span data-stu-id="06a91-110">The enrollRenewalPKCS7 sample:</span></span>

1.  <span data-ttu-id="06a91-111">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="06a91-111">Processes the command line arguments.</span></span> <span data-ttu-id="06a91-112">La ligne de commande doit contenir le nom du modèle utilisé pour créer la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="06a91-112">The command line should contain the name of the template used to create the certificate request.</span></span>
2.  <span data-ttu-id="06a91-113">Récupère un certificat existant en utilisant le nom du modèle spécifié sur la ligne de commande ou, si un certificat est introuvable, tente d’en inscrire un à l’aide du modèle.</span><span class="sxs-lookup"><span data-stu-id="06a91-113">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll one by using the template.</span></span> <span data-ttu-id="06a91-114">Les fonctions findCertByTemplate et enrollCertByTemplate sont définies dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="06a91-114">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="06a91-115">Vérifie la chaîne de certificats et convertit le certificat en **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="06a91-115">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="06a91-116">Crée un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) et l’initialise à l’aide du certificat existant.</span><span class="sxs-lookup"><span data-stu-id="06a91-116">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="06a91-117">Étant donné que le paramètre *inheritOptions* est défini sur InheritDefault, une nouvelle paire de clés est créée pour la demande, mais le fournisseur de services de chiffrement dans le certificat existant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="06a91-117">Because the *inheritOptions* parameter is set to InheritDefault, a new key pair is created for the request but the cryptographic provider in the existing certificate is used.</span></span> <span data-ttu-id="06a91-118">Pour plus d’informations, consultez la méthode [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .</span><span class="sxs-lookup"><span data-stu-id="06a91-118">For more information, see the [**InitializeFromCertificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) method.</span></span>
5.  <span data-ttu-id="06a91-119">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l' \# objet de requête PKCS 7, tente de l’inscrire auprès de l’autorité de certification et surveille l’état du processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="06a91-119">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="06a91-120">La fonction checkEnrollStatus est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="06a91-120">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06a91-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="06a91-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a91-122">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="06a91-122">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="06a91-123">\#Demande de renouvellement PKCS 7</span><span class="sxs-lookup"><span data-stu-id="06a91-123">PKCS \#7 Renewal Request</span></span>](pkcs--7--renewal-request.md)
</dt> <dt>

[<span data-ttu-id="06a91-124">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="06a91-124">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



