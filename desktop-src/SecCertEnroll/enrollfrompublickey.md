---
description: Initialise un objet de \# demande de certificat PKCS 10, l’encapsule dans un objet de demande CMC, soumet la demande CMC à une autorité de certification d’entreprise (ca) et enregistre le certificat retourné par l’autorité de certification dans un fichier.
ms.assetid: 0231da3b-a183-4443-8735-5affd24b145a
title: enrollFromPublicKey
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b336d04727f4bb4b90674bad6bb6c429465a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752725"
---
# <a name="enrollfrompublickey"></a><span data-ttu-id="2bb12-103">enrollFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="2bb12-103">enrollFromPublicKey</span></span>

<span data-ttu-id="2bb12-104">L’exemple enrollFromPublicKey Initialise un objet de \# demande de certificat PKCS 10, l’encapsule dans un objet de demande CMC, soumet la demande CMC à une autorité de certification d’entreprise (ca) et enregistre le certificat retourné par l’autorité de certification dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="2bb12-104">The enrollFromPublicKey sample initializes a PKCS \#10 certificate request object, wraps it in a CMC request object, submits the CMC request to an enterprise certification authority (CA), and saves the certificate returned by the CA in a file.</span></span>

## <a name="location"></a><span data-ttu-id="2bb12-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="2bb12-105">Location</span></span>

<span data-ttu-id="2bb12-106">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollFromPublicKey VC.</span><span class="sxs-lookup"><span data-stu-id="2bb12-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollFromPublicKey folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="2bb12-107">Discussions</span><span class="sxs-lookup"><span data-stu-id="2bb12-107">Discussion</span></span>

<span data-ttu-id="2bb12-108">Exemple enrollFromPublicKey :</span><span class="sxs-lookup"><span data-stu-id="2bb12-108">The enrollFromPublicKey sample:</span></span>

1.  <span data-ttu-id="2bb12-109">Traite les arguments de ligne de commande suivants :</span><span class="sxs-lookup"><span data-stu-id="2bb12-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="2bb12-110">Nom d’un modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="2bb12-110">The name of a certificate template.</span></span>
    -   <span data-ttu-id="2bb12-111">Nom d’un fichier dans lequel enregistrer le certificat installé sous la forme d’un tableau d’octets encodé en base64.</span><span class="sxs-lookup"><span data-stu-id="2bb12-111">The name of a file in which to save the installed certificate as a base64-encoded byte array.</span></span>
    -   <span data-ttu-id="2bb12-112">Nom de modèle de certificat de signature facultatif.</span><span class="sxs-lookup"><span data-stu-id="2bb12-112">An optional signing certificate template name.</span></span> <span data-ttu-id="2bb12-113">Le modèle est utilisé pour créer un certificat de signature s’il n’en existe aucun dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="2bb12-113">The template is used to create a signing certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="2bb12-114">Crée un objet de clé privée [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) et appelle la méthode [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) pour créer une clé privée asymétrique à l’aide du fournisseur de services de chiffrement par défaut, de la taille de la clé et des valeurs [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) pour l’ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="2bb12-114">Creates an [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) private key object and calls the [**Create**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create) method to create an asymmetric private key using the default cryptographic provider, key size, and [**KeySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) values for the current computer.</span></span>
3.  <span data-ttu-id="2bb12-115">Récupère la partie clé publique de l’objet [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .</span><span class="sxs-lookup"><span data-stu-id="2bb12-115">Retrieves the public key portion of the [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) object.</span></span>
4.  <span data-ttu-id="2bb12-116">Crée un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise à l’aide du modèle spécifié sur la ligne de commande et de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="2bb12-116">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object and initializes it by using the template specified on the command line and the public key.</span></span>
5.  <span data-ttu-id="2bb12-117">Crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise à l’aide de l' \# objet de requête PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="2bb12-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the PKCS \#10 request object.</span></span>
6.  <span data-ttu-id="2bb12-118">Récupère un certificat de signature existant ou, si celui-ci est introuvable, crée une demande de certificat à partir du modèle spécifié sur la ligne de commande et tente de l’inscrire.</span><span class="sxs-lookup"><span data-stu-id="2bb12-118">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="2bb12-119">FindCertByKeyUsage est défini dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="2bb12-119">The findCertByKeyUsage is defined in enrollCommon.cpp.</span></span>
7.  <span data-ttu-id="2bb12-120">Vérifie la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="2bb12-120">Verifies the certificate chain.</span></span>
8.  <span data-ttu-id="2bb12-121">Crée un objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat de signature, récupère la collection [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de l’objet de demande CMC et ajoute l’objet de certificat de signature à la collection.</span><span class="sxs-lookup"><span data-stu-id="2bb12-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the signing certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the signing certificate object to the collection.</span></span>
9.  <span data-ttu-id="2bb12-122">Encode la demande CMC à l’aide d' [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der).</span><span class="sxs-lookup"><span data-stu-id="2bb12-122">Encodes the CMC request by using [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER).</span></span>
10. <span data-ttu-id="2bb12-123">Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="2bb12-123">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
11. <span data-ttu-id="2bb12-124">Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="2bb12-124">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
12. <span data-ttu-id="2bb12-125">Vérifie l’état du processus d’inscription et enregistre le certificat installé dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="2bb12-125">Checks the status of the enrollment process and saves the installed certificate to a file.</span></span> <span data-ttu-id="2bb12-126">La fonction EncodeToFileW est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="2bb12-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bb12-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2bb12-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bb12-128">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="2bb12-128">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="2bb12-129">\#Demande PKCS 10</span><span class="sxs-lookup"><span data-stu-id="2bb12-129">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="2bb12-130">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="2bb12-130">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
