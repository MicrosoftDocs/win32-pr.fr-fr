---
description: Le kit de développement logiciel (SDK) d’inscription de certificats peut être utilisé pour créer des \# demandes de certificat PKCS 10, PKCS \# 7, CMC et auto-signé.
ms.assetid: 218eafb9-c9c8-49ff-8288-3909ed708ffc
title: Demandes de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690f3a5117abfa0ae262f0a8fa38f68528abf02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516045"
---
# <a name="certificate-requests"></a><span data-ttu-id="3c15c-103">Demandes de certificat</span><span class="sxs-lookup"><span data-stu-id="3c15c-103">Certificate Requests</span></span>

<span data-ttu-id="3c15c-104">Le kit de développement logiciel (SDK) d’inscription de certificats peut être utilisé pour créer des \# demandes de certificat PKCS 10, PKCS \# 7, CMC et auto-signé.</span><span class="sxs-lookup"><span data-stu-id="3c15c-104">The Certificate Enrollment SDK can be used to create PKCS \#10, PKCS \#7, CMC, and self-signed certificate requests.</span></span> <span data-ttu-id="3c15c-105">Chaque type de requête est représenté par l’une des interfaces énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3c15c-105">Each type of request is represented by one of the interfaces listed in the following table.</span></span> <span data-ttu-id="3c15c-106">Toutes les interfaces de requête héritent directement ou indirectement de l’interface [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) .</span><span class="sxs-lookup"><span data-stu-id="3c15c-106">All request interfaces inherit directly or indirectly from the [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) interface.</span></span> 

| <span data-ttu-id="3c15c-107">Interface</span><span class="sxs-lookup"><span data-stu-id="3c15c-107">Interface</span></span>                                                                        | <span data-ttu-id="3c15c-108">Description</span><span class="sxs-lookup"><span data-stu-id="3c15c-108">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c15c-109">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="3c15c-109">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | <span data-ttu-id="3c15c-110">Représente une \# demande PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="3c15c-110">Represents a PKCS \#10 request.</span></span> <span data-ttu-id="3c15c-111">Cette interface hérite de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="3c15c-111">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                   |
| [<span data-ttu-id="3c15c-112">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="3c15c-112">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | <span data-ttu-id="3c15c-113">Représente une \# demande PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="3c15c-113">Represents a PKCS \#7 request.</span></span> <span data-ttu-id="3c15c-114">Cette interface hérite de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span><span class="sxs-lookup"><span data-stu-id="3c15c-114">This interface inherits from [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).</span></span>                    |
| [<span data-ttu-id="3c15c-115">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="3c15c-115">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | <span data-ttu-id="3c15c-116">Représente un certificat auto-signé.</span><span class="sxs-lookup"><span data-stu-id="3c15c-116">Represents a self-signed certificate.</span></span> <span data-ttu-id="3c15c-117">Cette interface hérite de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span><span class="sxs-lookup"><span data-stu-id="3c15c-117">This interface inherits from [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10).</span></span> |
| [<span data-ttu-id="3c15c-118">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="3c15c-118">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | <span data-ttu-id="3c15c-119">Représente une demande CMC.</span><span class="sxs-lookup"><span data-stu-id="3c15c-119">Represents a CMC request.</span></span> <span data-ttu-id="3c15c-120">Cette interface hérite de [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span><span class="sxs-lookup"><span data-stu-id="3c15c-120">This interface inherits from [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).</span></span>               |



 

<span data-ttu-id="3c15c-121">L’illustration suivante montre la structure d’héritage des objets de requête pris en charge par l’API d’inscription de certificats.</span><span class="sxs-lookup"><span data-stu-id="3c15c-121">The following illustration shows the inheritance structure of the request objects supported by the Certificate Enrollment API.</span></span> <span data-ttu-id="3c15c-122">Un objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) sert, directement ou indirectement, à la classe de base pour tous les objets de requête disponibles.</span><span class="sxs-lookup"><span data-stu-id="3c15c-122">An [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) object serves, directly or indirectly, as the base class for all of the available request objects.</span></span>

![structure d’héritage pour les interfaces de demande](images/certificate-request-inheritance.png)

<span data-ttu-id="3c15c-124">Quel que soit le type, une demande de certificat contient des informations sur l’objet qui effectue la demande, la clé publique du sujet, un ensemble d’attributs, un ensemble d’extensions X. 509 version 3 (qui peuvent être envoyées dans le cadre des attributs) et une signature.</span><span class="sxs-lookup"><span data-stu-id="3c15c-124">Regardless of type, a certificate request contains information about the subject making the request, the subject's public key, a set of attributes, a set of X.509 version 3 extensions (which may be submitted as part of the attributes), and a signature.</span></span> <span data-ttu-id="3c15c-125">Ces problèmes sont traités dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c15c-125">These issues are addressed by the following topics:</span></span>

-   [<span data-ttu-id="3c15c-126">Noms de sujets</span><span class="sxs-lookup"><span data-stu-id="3c15c-126">Subject Names</span></span>](subject-names.md)
-   [<span data-ttu-id="3c15c-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="3c15c-127">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="3c15c-128">Extensions</span><span class="sxs-lookup"><span data-stu-id="3c15c-128">Extensions</span></span>](extensions.md)

## <a name="related-topics"></a><span data-ttu-id="3c15c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c15c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c15c-130">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="3c15c-130">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[<span data-ttu-id="3c15c-131">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="3c15c-131">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[<span data-ttu-id="3c15c-132">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="3c15c-132">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[<span data-ttu-id="3c15c-133">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="3c15c-133">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



