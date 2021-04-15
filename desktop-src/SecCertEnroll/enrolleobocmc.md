---
description: Crée une demande de certificat CMC pour le compte d’un autre utilisateur et inscrit l’utilisateur dans une hiérarchie de certificats.
ms.assetid: 14cc76c9-0e2b-498f-b058-244af6e9111e
title: enrollEOBOCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca888d949054d695056d42045335f17dfca2f4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526992"
---
# <a name="enrolleobocmc"></a><span data-ttu-id="c8042-103">enrollEOBOCMC</span><span class="sxs-lookup"><span data-stu-id="c8042-103">enrollEOBOCMC</span></span>

<span data-ttu-id="c8042-104">L’exemple enrollEOBOCMC crée une demande de certificat CMC pour le compte d’un autre utilisateur et inscrit l’utilisateur dans une hiérarchie de certificats.</span><span class="sxs-lookup"><span data-stu-id="c8042-104">The enrollEOBOCMC sample creates a CMC certificate request on behalf of another user and enrolls the user in a certificate hierarchy.</span></span> <span data-ttu-id="c8042-105">L’inscription pour le compte d’un autre utilisateur nécessite que la demande de certificat soit signée à l’aide d’un certificat d’agent d’inscription.</span><span class="sxs-lookup"><span data-stu-id="c8042-105">Enrollment on behalf of another user requires that the certificate request be signed by using an enrollment agent certificate.</span></span>

## <a name="location"></a><span data-ttu-id="c8042-106">Emplacement</span><span class="sxs-lookup"><span data-stu-id="c8042-106">Location</span></span>

<span data-ttu-id="c8042-107">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollEOBOCMC VC.</span><span class="sxs-lookup"><span data-stu-id="c8042-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollEOBOCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="c8042-108">Discussions</span><span class="sxs-lookup"><span data-stu-id="c8042-108">Discussion</span></span>

<span data-ttu-id="c8042-109">Exemple enrollEOBOCMC :</span><span class="sxs-lookup"><span data-stu-id="c8042-109">The enrollEOBOCMC sample:</span></span>

1.  <span data-ttu-id="c8042-110">Traite les arguments de ligne de commande suivants :</span><span class="sxs-lookup"><span data-stu-id="c8042-110">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="c8042-111">Nom d’un modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="c8042-111">The name of a certificate template.</span></span>
    -   <span data-ttu-id="c8042-112">Nom de l’utilisateur qui demande le certificat.</span><span class="sxs-lookup"><span data-stu-id="c8042-112">The name of the user requesting the certificate.</span></span>
    -   <span data-ttu-id="c8042-113">Nom d’un fichier d’échange d’informations personnelles (PFX) dans lequel enregistrer la demande.</span><span class="sxs-lookup"><span data-stu-id="c8042-113">The name of a Personal Information Exchange (PFX) file in which to save the request.</span></span>
    -   <span data-ttu-id="c8042-114">Mot de passe à utiliser avec le fichier PFX.</span><span class="sxs-lookup"><span data-stu-id="c8042-114">A password to use with the PFX file.</span></span>
    -   <span data-ttu-id="c8042-115">Nom de modèle d’agent d’inscription facultatif.</span><span class="sxs-lookup"><span data-stu-id="c8042-115">An optional enrollment agent template name.</span></span> <span data-ttu-id="c8042-116">Le modèle est utilisé pour créer un certificat d’agent d’inscription s’il n’en existe aucun dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="c8042-116">The template is used to create an enrollment agent certificate if none exists in the certificate store.</span></span>
2.  <span data-ttu-id="c8042-117">Crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise à l’aide du modèle de certificat spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c8042-117">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object and initializes it by using the certificate template specified on the command line.</span></span>
3.  <span data-ttu-id="c8042-118">Ajoute le nom du demandeur à l’objet de demande CMC.</span><span class="sxs-lookup"><span data-stu-id="c8042-118">Adds the name of the requester to the CMC request object.</span></span>
4.  <span data-ttu-id="c8042-119">Récupère un certificat d’agent d’inscription existant ou, si celui-ci est introuvable, crée une demande de certificat à partir du modèle d’agent d’inscription spécifié sur la ligne de commande et tente de l’inscrire.</span><span class="sxs-lookup"><span data-stu-id="c8042-119">Retrieves an existing enrollment agent certificate or, if one cannot be found, creates a certificate request from the enrollment agent template specified on the command line and attempts to enroll it.</span></span>
5.  <span data-ttu-id="c8042-120">Vérifie la chaîne de certificats qui contient le certificat de l’agent d’inscription.</span><span class="sxs-lookup"><span data-stu-id="c8042-120">Verifies the certificate chain that contains the enrollment agent certificate.</span></span>
6.  <span data-ttu-id="c8042-121">Crée un objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat de l’agent d’inscription, récupère la collection [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de l’objet de demande CMC et ajoute l’objet certificat de signature de l’agent d’inscription à la collection.</span><span class="sxs-lookup"><span data-stu-id="c8042-121">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the enrollment agent certificate, retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the CMC request object, and adds the enrollment agent signing certificate object to the collection.</span></span> <span data-ttu-id="c8042-122">L’objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) abordé à l’étape suivante utilise le certificat pour signer la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="c8042-122">The [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object discussed in the next step uses the certificate to sign the CMC request.</span></span>
7.  <span data-ttu-id="c8042-123">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de la demande CMC, tente de l’inscrire et vérifie la progression du processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="c8042-123">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, attempts to enroll it, and checks the progress of the enrollment process.</span></span>
8.  <span data-ttu-id="c8042-124">Exporte le certificat installé vers un fichier PFX.</span><span class="sxs-lookup"><span data-stu-id="c8042-124">Exports the installed certificate to a PFX file.</span></span> <span data-ttu-id="c8042-125">Le fichier est protégé à l’aide du mot de passe spécifié sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c8042-125">The file is protected by using the password specified on the command line.</span></span> <span data-ttu-id="c8042-126">La fonction EncodeToFileW est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="c8042-126">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>
9.  <span data-ttu-id="c8042-127">Supprime le certificat du magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="c8042-127">Deletes the certificate from the certificate store.</span></span> <span data-ttu-id="c8042-128">Les fonctions utilisées dans l’exemple de code suivant se trouvent dans la documentation CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="c8042-128">The functions used in the following code example can be found in the CryptoAPI documentation.</span></span>
10. <span data-ttu-id="c8042-129">Supprime la clé privée de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c8042-129">Deletes the private key from the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8042-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8042-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8042-131">Demande EOBO CMC</span><span class="sxs-lookup"><span data-stu-id="c8042-131">CMC EOBO Request</span></span>](cmc-eobo-request.md)
</dt> <dt>

[<span data-ttu-id="c8042-132">\#Demande PKCS 10</span><span class="sxs-lookup"><span data-stu-id="c8042-132">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="c8042-133">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="c8042-133">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



