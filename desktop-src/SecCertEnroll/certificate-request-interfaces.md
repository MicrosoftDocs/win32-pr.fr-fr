---
description: Les interfaces suivantes peuvent être utilisées pour créer des demandes de certificat.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfaces de demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e18a4f8e1ce60348ffdf52afe210247f6d20a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113775"
---
# <a name="certificate-request-interfaces"></a><span data-ttu-id="3dea1-103">Interfaces de demande de certificat</span><span class="sxs-lookup"><span data-stu-id="3dea1-103">Certificate Request Interfaces</span></span>

<span data-ttu-id="3dea1-104">Les interfaces suivantes peuvent être utilisées pour créer des demandes de certificat.</span><span class="sxs-lookup"><span data-stu-id="3dea1-104">The following interfaces can be used to create certificate requests.</span></span>



| <span data-ttu-id="3dea1-105">Interface</span><span class="sxs-lookup"><span data-stu-id="3dea1-105">Interface</span></span>                                                                          | <span data-ttu-id="3dea1-106">Description</span><span class="sxs-lookup"><span data-stu-id="3dea1-106">Description</span></span>                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dea1-107">**IX509CertificateRequest**</span><span class="sxs-lookup"><span data-stu-id="3dea1-107">**IX509CertificateRequest**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | <span data-ttu-id="3dea1-108">Représente l’interface abstraite de niveau supérieur pour une demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="3dea1-108">Represents the abstract top-level interface for a certificate request.</span></span>                                                                                        |
| [<span data-ttu-id="3dea1-109">**IX509CertificateRequestCertificate**</span><span class="sxs-lookup"><span data-stu-id="3dea1-109">**IX509CertificateRequestCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | <span data-ttu-id="3dea1-110">Vous permet de créer des certificats directement sans passer par une autorité d’inscription ou de certification.</span><span class="sxs-lookup"><span data-stu-id="3dea1-110">Enables you to create certificates directly without going through a registration or certification authority.</span></span>                                                  |
| [<span data-ttu-id="3dea1-111">**IX509CertificateRequestCertificate2**</span><span class="sxs-lookup"><span data-stu-id="3dea1-111">**IX509CertificateRequestCertificate2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | <span data-ttu-id="3dea1-112">Étend l’interface [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) pour permettre l’initialisation à partir d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="3dea1-112">Extends the [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) interface to enable initialization from a template.</span></span>              |
| [<span data-ttu-id="3dea1-113">**IX509CertificateRequestCmc**</span><span class="sxs-lookup"><span data-stu-id="3dea1-113">**IX509CertificateRequestCmc**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | <span data-ttu-id="3dea1-114">Représente une demande CMC.</span><span class="sxs-lookup"><span data-stu-id="3dea1-114">Represents a CMC request.</span></span>                                                                                                                                     |
| [<span data-ttu-id="3dea1-115">**IX509CertificateRequestCmc2**</span><span class="sxs-lookup"><span data-stu-id="3dea1-115">**IX509CertificateRequestCmc2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | <span data-ttu-id="3dea1-116">Étend l’interface [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) pour permettre l’initialisation à partir d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="3dea1-116">Extends the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) interface to enable initialization from a template.</span></span>                              |
| [<span data-ttu-id="3dea1-117">**IX509CertificateRequestPkcs10**</span><span class="sxs-lookup"><span data-stu-id="3dea1-117">**IX509CertificateRequestPkcs10**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | <span data-ttu-id="3dea1-118">Représente une \# demande PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="3dea1-118">Represents a PKCS \#10 request.</span></span>                                                                                                                               |
| [<span data-ttu-id="3dea1-119">**IX509CertificateRequestPkcs10V2**</span><span class="sxs-lookup"><span data-stu-id="3dea1-119">**IX509CertificateRequestPkcs10V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | <span data-ttu-id="3dea1-120">Étend l’interface [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) pour permettre l’initialisation à partir d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="3dea1-120">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface to enable initialization from a template.</span></span>                        |
| [<span data-ttu-id="3dea1-121">**IX509CertificateRequestPkcs10V3**</span><span class="sxs-lookup"><span data-stu-id="3dea1-121">**IX509CertificateRequestPkcs10V3**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | <span data-ttu-id="3dea1-122">Étend l’interface [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et ajoute des propriétés qui activent l’attestation de certificat TPM.</span><span class="sxs-lookup"><span data-stu-id="3dea1-122">Extends the [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) interface and adds properties that enable TPM certificate attestation.</span></span> |
| [<span data-ttu-id="3dea1-123">**IX509CertificateRequestPkcs7**</span><span class="sxs-lookup"><span data-stu-id="3dea1-123">**IX509CertificateRequestPkcs7**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | <span data-ttu-id="3dea1-124">Représente une \# demande PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="3dea1-124">Represents a PKCS \#7 request.</span></span>                                                                                                                                |
| [<span data-ttu-id="3dea1-125">**IX509CertificateRequestPkcs7V2**</span><span class="sxs-lookup"><span data-stu-id="3dea1-125">**IX509CertificateRequestPkcs7V2**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | <span data-ttu-id="3dea1-126">Étend l’interface [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) pour permettre l’initialisation à partir d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="3dea1-126">Extends the [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) interface to enable initialization from a template.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="3dea1-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3dea1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dea1-128">CertEnroll, interfaces</span><span class="sxs-lookup"><span data-stu-id="3dea1-128">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



