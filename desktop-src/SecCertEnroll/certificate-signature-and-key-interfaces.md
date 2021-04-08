---
description: Les interfaces suivantes peuvent être utilisées pour gérer des signatures de certificat et des clés publiques et privées.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Signature de certificat et interfaces clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866670"
---
# <a name="certificate-signature-and-key-interfaces"></a>Signature de certificat et interfaces clés

Les interfaces suivantes peuvent être utilisées pour gérer des signatures de certificat et des clés publiques et privées.



| Interface                                                      | Description                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Représente un certificat de signature qui vous permet de signer une demande de certificat.                  |
| [**ISignerCertificates**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Gère une collection d’objets [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Représente une clé privée asymétrique qui peut être utilisée pour le chiffrement, la signature et l’accord de clé. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Représente une clé publique dans une paire de clés publique/privée.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Représente les informations utilisées pour signer une demande de certificat.                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



