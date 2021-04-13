---
description: Lit une demande de certificat CMC existante à partir d’un fichier, l’encapsule dans une autre demande CMC, signe cette requête externe, la soumet à une autorité de certification (CA) et enregistre la réponse du certificat de l’autorité de certification dans un fichier.
ms.assetid: b1a9161d-1f9a-4c5b-acd2-6058dc65a258
title: enrollNestedCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1df25a1bc7f6ce16a67f66ff58dc371a526813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201242"
---
# <a name="enrollnestedcmc"></a><span data-ttu-id="93204-103">enrollNestedCMC</span><span class="sxs-lookup"><span data-stu-id="93204-103">enrollNestedCMC</span></span>

<span data-ttu-id="93204-104">L’exemple enrollNestedCMC lit une demande de certificat CMC existante à partir d’un fichier, l’encapsule dans une autre demande CMC, signe cette requête externe, la soumet à une autorité de certification (CA) et enregistre la réponse du certificat de l’autorité de certification dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="93204-104">The enrollNestedCMC sample reads an existing CMC certificate request from a file, wraps it in another CMC request, signs this outer request, submits it to a certification authority (CA), and saves the certificate response from the CA to a file.</span></span>

## <a name="location"></a><span data-ttu-id="93204-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="93204-105">Location</span></span>

<span data-ttu-id="93204-106">Lorsque vous installez le kit de développement logiciel (SDK) de Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples enrollNestedCMC de l' \\ inscription de certificats X509 \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="93204-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\X509 Certificate Enrollment\\VC\\enrollNestedCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="93204-107">Discussions</span><span class="sxs-lookup"><span data-stu-id="93204-107">Discussion</span></span>

<span data-ttu-id="93204-108">Exemple enrollNestedCMC :</span><span class="sxs-lookup"><span data-stu-id="93204-108">The enrollNestedCMC sample:</span></span>

1.  <span data-ttu-id="93204-109">Traite les arguments de ligne de commande suivants :</span><span class="sxs-lookup"><span data-stu-id="93204-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="93204-110">Nom du fichier d’entrée.</span><span class="sxs-lookup"><span data-stu-id="93204-110">The name of the input file.</span></span>
    -   <span data-ttu-id="93204-111">Nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="93204-111">The name of the output file.</span></span>
    -   <span data-ttu-id="93204-112">Modèle de demande facultatif.</span><span class="sxs-lookup"><span data-stu-id="93204-112">An optional request template.</span></span>
2.  <span data-ttu-id="93204-113">Lit une demande CMC existante à partir d’un fichier en tant que tableau d’octets encodé base63, convertit le tableau d’octets en **BSTR**, crée un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et utilise le **BSTR** pour initialiser l’objet de requête.</span><span class="sxs-lookup"><span data-stu-id="93204-113">Reads an existing CMC request from a file as a base63-encoded byte array, converts the byte array to a **BSTR**, creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object, and uses the **BSTR** to initialize the request object.</span></span> <span data-ttu-id="93204-114">L’objet initialisé devient la requête interne.</span><span class="sxs-lookup"><span data-stu-id="93204-114">The initialized object becomes the inner request.</span></span>
3.  <span data-ttu-id="93204-115">Utilise l’objet de requête interne créé et initialisé à l’étape précédente pour initialiser une autre demande CMC.</span><span class="sxs-lookup"><span data-stu-id="93204-115">Uses the inner request object created and initialized in the preceding step to initialize another CMC request.</span></span>
4.  <span data-ttu-id="93204-116">Récupère un certificat de signature existant ou, si celui-ci est introuvable, crée une demande de certificat à partir du modèle spécifié sur la ligne de commande et tente de l’inscrire.</span><span class="sxs-lookup"><span data-stu-id="93204-116">Retrieves an existing signing certificate or, if one cannot be found, creates a certificate request from the template specified on the command line and attempts to enroll it.</span></span> <span data-ttu-id="93204-117">Les fonctions findCertByTemplate et enrollCertByTemplate sont définies dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="93204-117">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
5.  <span data-ttu-id="93204-118">Récupère la collection [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) de la demande CMC externe, crée un nouvel objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat de signature récupéré et l’ajoute à la collection.</span><span class="sxs-lookup"><span data-stu-id="93204-118">Retrieves the [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates) collection from the outer CMC request, creates a new [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the retrieved signing certificate, and adds it to the collection.</span></span>
6.  <span data-ttu-id="93204-119">Encode la demande CMC à l’aide d’Distinguished Encoding Rules (DER) et récupère la requête en tant que **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="93204-119">Encodes the CMC request by using Distinguished Encoding Rules (DER) and retrieves the request as a **BSTR**.</span></span>
7.  <span data-ttu-id="93204-120">Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="93204-120">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
8.  <span data-ttu-id="93204-121">Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="93204-121">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
9.  <span data-ttu-id="93204-122">Vérifie l’état du processus d’inscription et enregistre la réponse du certificat de l’autorité de certification dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="93204-122">Checks the status of the enrollment process and saves the certificate response from the CA to a file.</span></span> <span data-ttu-id="93204-123">La fonction EncodeToFileW est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="93204-123">The EncodeToFileW function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93204-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93204-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93204-125">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="93204-125">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="93204-126">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="93204-126">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
