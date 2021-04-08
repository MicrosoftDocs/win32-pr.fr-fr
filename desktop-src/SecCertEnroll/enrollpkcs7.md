---
description: Crée une \# demande PKCS 7 à partir d’un certificat existant en héritant des clés publiques et privées et du modèle de certificat.
ms.assetid: e7df1a2e-5674-4cc6-874b-45bcc7e25127
title: enrollPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34bc7f9d7b7d5ae9fa88db0dd70c177c3aa69da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750020"
---
# <a name="enrollpkcs7"></a><span data-ttu-id="ddbf7-103">enrollPKCS7</span><span class="sxs-lookup"><span data-stu-id="ddbf7-103">enrollPKCS7</span></span>

<span data-ttu-id="ddbf7-104">L’exemple enrollPKCS7 crée une \# demande PKCS 7 à partir d’un certificat existant en héritant des clés publiques et privées et du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-104">The enrollPKCS7 sample creates a PKCS \#7 request from an existing certificate by inheriting the public and private keys and the certificate template.</span></span> <span data-ttu-id="ddbf7-105">Le certificat existant est utilisé pour signer la demande.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-105">The existing certificate is used to sign the request.</span></span> <span data-ttu-id="ddbf7-106">Cet exemple inscrit l’utilisateur dans une hiérarchie de certificats et installe la réponse du certificat.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-106">This sample enrolls the user in a certificate hierarchy and installs the certificate response.</span></span> <span data-ttu-id="ddbf7-107">L’exemple utilise un certificat existant pour inscrire et installer un nouveau certificat.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-107">The sample uses an existing certificate to enroll and install a new one.</span></span> <span data-ttu-id="ddbf7-108">Pour plus d’informations sur le renouvellement d’un certificat existant, consultez [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span><span class="sxs-lookup"><span data-stu-id="ddbf7-108">For more information about renewing an existing certificate, see [enrollRenewalPKCS7](enrollrenewalpkcs7.md).</span></span>

## <a name="location"></a><span data-ttu-id="ddbf7-109">Emplacement</span><span class="sxs-lookup"><span data-stu-id="ddbf7-109">Location</span></span>

<span data-ttu-id="ddbf7-110">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollPKCS7 VC.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-110">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollPKCS7 folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="ddbf7-111">Discussions</span><span class="sxs-lookup"><span data-stu-id="ddbf7-111">Discussion</span></span>

<span data-ttu-id="ddbf7-112">Exemple enrollPKCS7 :</span><span class="sxs-lookup"><span data-stu-id="ddbf7-112">The enrollPKCS7 sample:</span></span>

1.  <span data-ttu-id="ddbf7-113">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-113">Processes the command line arguments.</span></span> <span data-ttu-id="ddbf7-114">La ligne de commande doit contenir le nom du modèle de certificat utilisé pour rechercher un certificat existant.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-114">The command line should contain the name of the certificate template used to find an existing certificate.</span></span>
2.  <span data-ttu-id="ddbf7-115">Récupère un certificat existant en utilisant le nom du modèle spécifié sur la ligne de commande ou, si un certificat est introuvable, tente d’inscrire un nouveau certificat créé à l’aide du modèle.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-115">Retrieves an existing certificate by using the name of the template specified on the command line or, if a certificate cannot be found, attempts to enroll a new one created by using the template.</span></span> <span data-ttu-id="ddbf7-116">Les fonctions findCertByTemplate et enrollCertByTemplate sont définies dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-116">The findCertByTemplate and enrollCertByTemplate functions are defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="ddbf7-117">Vérifie la chaîne de certificats et convertit le certificat en **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-117">Verifies the certificate chain and converts the certificate to a **BSTR**.</span></span>
4.  <span data-ttu-id="ddbf7-118">Crée un objet [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) et l’initialise à l’aide du certificat existant.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-118">Creates an [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) object and initializes it by using the existing certificate.</span></span> <span data-ttu-id="ddbf7-119">Le nouvel \# objet de requête PKCS 7 hérite des clés et du modèle privés et publics du certificat existant.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-119">The new PKCS \#7 request object inherits the private and public keys and template from the existing certificate.</span></span>
5.  <span data-ttu-id="ddbf7-120">Crée un objet [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) , l’initialise à l’aide du certificat existant et l’ajoute à l’objet de \# requête PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-120">Creates an [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) object, initializes it by using the existing certificate, and adds it to the PKCS \#7 request object.</span></span>
6.  <span data-ttu-id="ddbf7-121">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de l' \# objet de requête PKCS 7, tente de l’inscrire auprès de l’autorité de certification et surveille l’état du processus d’inscription.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-121">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the PKCS \#7 request object, attempts to enroll it with the CA and monitors the status of the enrollment process.</span></span> <span data-ttu-id="ddbf7-122">La fonction checkEnrollStatus est définie dans enrollCommon. cpp.</span><span class="sxs-lookup"><span data-stu-id="ddbf7-122">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddbf7-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ddbf7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddbf7-124">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="ddbf7-124">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="ddbf7-125">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="ddbf7-125">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



