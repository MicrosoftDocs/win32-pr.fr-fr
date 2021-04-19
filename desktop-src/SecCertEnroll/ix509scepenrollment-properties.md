---
description: L’interface IX509SCEPEnrollment expose les propriétés suivantes.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Propriétés IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520616"
---
# <a name="ix509scepenrollment-properties"></a>Propriétés IX509SCEPEnrollment

L’interface [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) expose les propriétés suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                              | Description                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriété du certificat**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | Obtient le certificat pour la demande.<br/>                                                                                                       |
| [**Propriété CertificateFriendlyName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | Obtient ou définit le nom convivial du certificat.<br/>                                                                                         |
| [**Propriété FailInfo**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | Obtient des informations lorsque la méthode [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) détecte un environnement défaillant.<br/> |
| [**Propriété OldCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | Obtient ou définit un ancien certificat qu’une demande doit remplacer.<br/>                                                                      |
| [**Propriété de la demande**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | Obtient la demande interne PKCS10.<br/>                                                                                                              |
| [**Propriété ServerCapabilities**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | Définit les algorithmes de chiffrement et de hachage par défaut pour la demande.<br/>                                                                          |
| [**Propriété SignerCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | Obtient ou définit le certificat de signataire pour la demande.<br/>                                                                                        |
| [**Silent, propriété**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | Obtient ou définit une valeur indiquant s’il faut autoriser l’interface utilisateur pendant la requête.<br/>                                                                                        |
| [**Status (propriété)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | Obtient l’état de la demande.<br/>                                                                                                             |
| [**Propriété TransactionId**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | Obtient ou définit l’ID de transaction de la demande.<br/>                                                                                            |



 

 

 




