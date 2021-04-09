---
description: L’interface IX509CertificateRequestPkcs10V3 expose les propriétés suivantes.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Propriétés IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4967b10e49ed015b22ffcab19726f5662937d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953002"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Propriétés IX509CertificateRequestPkcs10V3

L’interface [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) expose les propriétés suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriété AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Certificat utilisé pour chiffrer les valeurs EKPUB et EKCERT à partir du client. Cette propriété doit être définie sur un certificat valide qui est lié à une racine d’ordinateur approuvé.<br/>                                                                                                                                                                                |
| [**Propriété AttestPrivateKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | True si la clé privée créée doit être sanctionnée ; Sinon, false. Si la valeur est true, la propriété [**AttestationEncryptionCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) est supposée être définie. <br/>                                                                                                        |
| [**Propriété ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Mot de passe à utiliser lors de la création d’une demande avec un challenge. Pour créer une demande sans problème, ne définissez pas la propriété [**ChallengePassword**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) .<br/>                                                                                                                                      |
| [**Propriété EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Algorithme de chiffrement utilisé pour chiffrer les valeurs EKPUB et EKCERT à partir du client.<br/>                                                                                                                                                                                                                                                               |
| [**Propriété EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Identifie la longueur en bits de l' [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) à utiliser pour le chiffrement. Si le **EncryptionAlgorithm** prend uniquement en charge une longueur de bit, vous n’avez pas besoin de spécifier une valeur pour la propriété [**EncryptionStrength**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) .<br/> |
| [**Propriété NameValuePairs**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Collection de paires nom/valeur de valeurs de propriété de certificat supplémentaires.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




