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
# <a name="certificate-requests"></a>Demandes de certificat

Le kit de développement logiciel (SDK) d’inscription de certificats peut être utilisé pour créer des \# demandes de certificat PKCS 10, PKCS \# 7, CMC et auto-signé. Chaque type de requête est représenté par l’une des interfaces énumérées dans le tableau suivant. Toutes les interfaces de requête héritent directement ou indirectement de l’interface [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) . 

| Interface                                                                        | Description                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)           | Représente une \# demande PKCS 10. Cette interface hérite de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                   |
| [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)             | Représente une \# demande PKCS 7. Cette interface hérite de [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest).                    |
| [**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate) | Représente un certificat auto-signé. Cette interface hérite de [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10). |
| [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)                 | Représente une demande CMC. Cette interface hérite de [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7).               |



 

L’illustration suivante montre la structure d’héritage des objets de requête pris en charge par l’API d’inscription de certificats. Un objet [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) sert, directement ou indirectement, à la classe de base pour tous les objets de requête disponibles.

![structure d’héritage pour les interfaces de demande](images/certificate-request-inheritance.png)

Quel que soit le type, une demande de certificat contient des informations sur l’objet qui effectue la demande, la clé publique du sujet, un ensemble d’attributs, un ensemble d’extensions X. 509 version 3 (qui peuvent être envoyées dans le cadre des attributs) et une signature. Ces problèmes sont traités dans les rubriques suivantes :

-   [Noms de sujets](subject-names.md)
-   [Attributs](attributes.md)
-   [Extensions](extensions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)
</dt> <dt>

[**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
</dt> <dt>

[**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
</dt> <dt>

[**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10)
</dt> </dl>

 

 



