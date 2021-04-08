---
description: Crée une demande de certificat CMC et inscrit un ordinateur dans une hiérarchie de certificats.
ms.assetid: ef09ef04-8925-4d66-97ad-70b4d7cf78b9
title: enrollCustomCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2910e6a6ca784aaeb9ca97dc8de106932bd64c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752733"
---
# <a name="enrollcustomcmc"></a><span data-ttu-id="4861a-103">enrollCustomCMC</span><span class="sxs-lookup"><span data-stu-id="4861a-103">enrollCustomCMC</span></span>

<span data-ttu-id="4861a-104">L’exemple enrollCustomCMC crée une demande de certificat CMC et inscrit un ordinateur dans une hiérarchie de certificats.</span><span class="sxs-lookup"><span data-stu-id="4861a-104">The enrollCustomCMC sample creates a CMC certificate request and enrolls a computer in a certificate hierarchy.</span></span>

## <a name="location"></a><span data-ttu-id="4861a-105">Emplacement</span><span class="sxs-lookup"><span data-stu-id="4861a-105">Location</span></span>

<span data-ttu-id="4861a-106">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollCustomCMC VC.</span><span class="sxs-lookup"><span data-stu-id="4861a-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollCustomCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="4861a-107">Discussions</span><span class="sxs-lookup"><span data-stu-id="4861a-107">Discussion</span></span>

<span data-ttu-id="4861a-108">Exemple enrollCustomCMC :</span><span class="sxs-lookup"><span data-stu-id="4861a-108">The enrollCustomCMC sample:</span></span>

1.  <span data-ttu-id="4861a-109">Traite les arguments de ligne de commande suivants :</span><span class="sxs-lookup"><span data-stu-id="4861a-109">Processes the following command line arguments:</span></span>
    -   <span data-ttu-id="4861a-110">Paire nom/valeur personnalisée à ajouter à la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="4861a-110">A custom name/value pair to add to the certificate request.</span></span>
    -   <span data-ttu-id="4861a-111">Autre nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4861a-111">An alternative subject name.</span></span>
    -   <span data-ttu-id="4861a-112">Identificateur d’objet (OID) pour l’extension d’utilisation améliorée de la clé.</span><span class="sxs-lookup"><span data-stu-id="4861a-112">An object identifier (OID) for the Enhanced Key Usage (EKU) extension.</span></span>
2.  <span data-ttu-id="4861a-113">Crée un objet de requête [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et l’initialise à l’aide du contexte de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4861a-113">Creates an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) request object and initializes it by using the computer context.</span></span>
3.  <span data-ttu-id="4861a-114">Utilise la \# requête PKCS 10 pour initialiser un objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="4861a-114">Uses the PKCS \#10 request to initialize an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
4.  <span data-ttu-id="4861a-115">Crée un objet [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) à l’aide de l’OID spécifié sur la ligne de commande et l’ajoute à la collection d’extensions pour la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="4861a-115">Creates an [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage) object by using the OID specified on the command line and adds it to the extensions collection for the CMC request.</span></span>
5.  <span data-ttu-id="4861a-116">Crée un objet [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) en utilisant le nom spécifié sur la ligne de commande, l’ajoute à la collection [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) , utilise la collection pour initialiser une extension [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) et l’ajoute à la collection d’extensions pour la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="4861a-116">Creates [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) object by using the name specified on the command line, adds it to the [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames) collection, uses the collection to initialize an [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames) extension and adds this to the extensions collection for the CMC request.</span></span>
6.  <span data-ttu-id="4861a-117">Crée un objet [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) en utilisant le nom et la valeur spécifiés sur la ligne de commande et l’ajoute à la collection [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) sur la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="4861a-117">Creates an [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) object by using the name and value specified on the command line, and adds it to the [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs) collection on the CMC request.</span></span>
7.  <span data-ttu-id="4861a-118">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l’objet de demande CMC et récupère une chaîne qui contient une demande encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="4861a-118">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request object, and retrieves a string that contains a base64-encoded request.</span></span>
8.  <span data-ttu-id="4861a-119">Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4861a-119">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and use it to retrieve a string that contains the CA configuration.</span></span>
9.  <span data-ttu-id="4861a-120">Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise, ainsi que les chaînes qui contiennent la configuration de l’autorité de certification et la demande de certificat pour envoyer la demande à l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4861a-120">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it plus the strings that contain the CA configuration and the certificate request to submit the request to the CA.</span></span>
10. <span data-ttu-id="4861a-121">Vérifie l’état de l’envoi et, en cas de réussite, installe le certificat dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="4861a-121">Checks the submission status and, if successful, installs the certificate to the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4861a-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4861a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4861a-123">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="4861a-123">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="4861a-124">\#Demande PKCS 10</span><span class="sxs-lookup"><span data-stu-id="4861a-124">PKCS \#10 Request</span></span>](pkcs--10-request.md)
</dt> <dt>

[<span data-ttu-id="4861a-125">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="4861a-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
