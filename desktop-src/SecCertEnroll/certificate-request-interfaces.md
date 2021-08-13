---
description: Les interfaces suivantes peuvent être utilisées pour créer des demandes de certificat.
ms.assetid: 6021db79-ac90-4e0c-afbd-0f926abcab78
title: Interfaces de demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba4f16c6aba1be724fcf2639dd64d7988e40b79a5b29a2d500beb3ae66f4ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902558"
---
# <a name="certificate-request-interfaces"></a>Interfaces de demande de certificat

Les interfaces suivantes peuvent être utilisées pour créer des demandes de certificat.



| Interface                                                                          | Description                                                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest)                         | Représente l’interface abstraite de niveau supérieur pour une demande de certificat.                                                                                        |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)   | Vous permet de créer des certificats directement sans passer par une autorité d’inscription ou de certification.                                                  |
| [**IX509CertificateRequestCertificate2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcertificate2) | Étend l’interface [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) pour permettre l’initialisation à partir d’un modèle.              |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                   | Représente une demande CMC.                                                                                                                                     |
| [**IX509CertificateRequestCmc2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestcmc2)                 | Étend l’interface [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) pour permettre l’initialisation à partir d’un modèle.                              |
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)             | Représente une \# demande PKCS 10.                                                                                                                               |
| [**IX509CertificateRequestPkcs10V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v2)         | Étend l’interface [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) pour permettre l’initialisation à partir d’un modèle.                        |
| [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3)         | Étend l’interface [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) et ajoute des propriétés qui activent l’attestation de certificat TPM. |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)               | Représente une \# demande PKCS 7.                                                                                                                                |
| [**IX509CertificateRequestPkcs7V2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs7v2)           | Étend l’interface [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) pour permettre l’initialisation à partir d’un modèle.                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



