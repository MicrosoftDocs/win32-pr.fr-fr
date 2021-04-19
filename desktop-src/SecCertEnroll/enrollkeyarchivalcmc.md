---
description: Crée une demande de certificat CMC pour archiver une clé privée sur une autorité de certification.
ms.assetid: b063989a-fe92-4c2c-9d66-8a14bc830f6b
title: enrollKeyArchivalCMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144f5f063834c156da5058fbc34f66ebdb76eb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520378"
---
# <a name="enrollkeyarchivalcmc"></a><span data-ttu-id="4a608-103">enrollKeyArchivalCMC</span><span class="sxs-lookup"><span data-stu-id="4a608-103">enrollKeyArchivalCMC</span></span>

<span data-ttu-id="4a608-104">L’exemple enrollKeyArchivalCMC crée une demande de certificat CMC pour archiver une clé privée sur une autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4a608-104">The enrollKeyArchivalCMC sample creates a CMC certificate request to archive a private key on a certification authority (CA).</span></span> <span data-ttu-id="4a608-105">Pour plus d’informations, consultez [demande d’archivage de clé CMC](cmc-key-archival-request.md).</span><span class="sxs-lookup"><span data-stu-id="4a608-105">For more information, see [CMC Key Archival Request](cmc-key-archival-request.md).</span></span>

## <a name="location"></a><span data-ttu-id="4a608-106">Emplacement</span><span class="sxs-lookup"><span data-stu-id="4a608-106">Location</span></span>

<span data-ttu-id="4a608-107">Lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows, l’exemple est installé, par défaut, dans le dossier *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ x509 Certificate \\ \\ enrollKeyArchivalCMC VC.</span><span class="sxs-lookup"><span data-stu-id="4a608-107">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\enrollKeyArchivalCMC folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="4a608-108">Discussions</span><span class="sxs-lookup"><span data-stu-id="4a608-108">Discussion</span></span>

<span data-ttu-id="4a608-109">Exemple enrollKeyArchivalCMC :</span><span class="sxs-lookup"><span data-stu-id="4a608-109">The enrollKeyArchivalCMC sample:</span></span>

1.  <span data-ttu-id="4a608-110">Traite les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4a608-110">Processes the command line arguments.</span></span> <span data-ttu-id="4a608-111">La ligne de commande doit contenir le nom du modèle de certificat à utiliser pour l’inscription.</span><span class="sxs-lookup"><span data-stu-id="4a608-111">The command line should contain the name of the certificate template to use for enrollment.</span></span>
2.  <span data-ttu-id="4a608-112">Crée un objet de demande de certificat [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) et l’initialise pour un contexte d’utilisateur final en utilisant le nom du modèle.</span><span class="sxs-lookup"><span data-stu-id="4a608-112">Creates an [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) certificate request object and initializes it for an end-user context by using the template name.</span></span>
3.  <span data-ttu-id="4a608-113">Définit la propriété [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) sur la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="4a608-113">Sets the [**ArchivePrivateKey**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_archiveprivatekey) property on the CMC request.</span></span>
4.  <span data-ttu-id="4a608-114">Crée un objet [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) et l’utilise pour récupérer une chaîne qui contient la configuration de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4a608-114">Creates an [**ICertConfig**](/windows/desktop/api/certcli/nn-certcli-icertconfig) object and uses it to retrieve a string that contains the CA configuration.</span></span>
5.  <span data-ttu-id="4a608-115">Crée un objet CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) et l’utilise pour récupérer le certificat Exchange pour l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4a608-115">Creates a CryptoAPI [**ICertRequest2**](/windows/desktop/api/certcli/nn-certcli-icertrequest2) object and uses it to retrieve the exchange certificate for the CA.</span></span>
6.  <span data-ttu-id="4a608-116">Crée un objet [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , l’initialise à l’aide de la demande CMC, crée une chaîne encodée en base64 qui contient la demande d’archivage de clé et l’envoie à l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="4a608-116">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object, initializes it by using the CMC request, creates a base64 encoded string that contains the key archival request, and submits it to the CA.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a608-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a608-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a608-118">Demande d’archivage de clé CMC</span><span class="sxs-lookup"><span data-stu-id="4a608-118">CMC Key Archival Request</span></span>](cmc-key-archival-request.md)
</dt> <dt>

[<span data-ttu-id="4a608-119">Demande CMC</span><span class="sxs-lookup"><span data-stu-id="4a608-119">CMC Request</span></span>](cmc-request.md)
</dt> <dt>

[<span data-ttu-id="4a608-120">Utilisation des exemples inclus</span><span class="sxs-lookup"><span data-stu-id="4a608-120">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 
