---
description: Les interfaces suivantes peuvent être utilisées pour gérer des signatures de certificat et des clés publiques et privées.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Signature de certificat et interfaces clés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdfd4c76b0e73f2954780d797e092e6d8b7570ebaee082ef93319f74abc24e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902305"
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

 

 



