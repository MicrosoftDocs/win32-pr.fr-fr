---
description: L’interface IX509EndorsementKey expose les méthodes suivantes.
ms.assetid: 536E5DE6-FF14-45C8-9227-68AF673E5FDC
title: Méthodes IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c1eb6a96cd555d4b0a0fdcd2ad52ccf80ec4aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210580"
---
# <a name="ix509endorsementkey-methods"></a>Méthodes IX509EndorsementKey

L’interface [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) expose les méthodes suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                        | Description                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Méthode AddCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-addcertificate)<br/>               | Ajoutez un certificat de clé de type EK au fournisseur de stockage de clés (KSP) qui prend en charge les clés de type EK.<br/>                                                                                                                                                                                     |
| [**Close, méthode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close)<br/>                                 | Ferme la clé de type EK. Vous pouvez appeler la méthode [**Close**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-close) uniquement après l’appel de la méthode [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .<br/>                                                                                              |
| [**Méthode ExportPublicKey**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-exportpublickey)<br/>             | Exporte la clé publique de la responsabilité.<br/>                                                                                                                                                                                                                                                      |
| [**Méthode GetCertificateByIndex**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatebyindex)<br/> | Obtient le certificat de responsabilité associé à la clé de type EK du fournisseur de stockage de clés pour l’index spécifié.<br/>                                                                                                                                                              |
| [**Méthode GetCertificateCount**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-getcertificatecount)<br/>     | Obtient le nombre de certificats de responsabilité dans le fournisseur de stockage de clés.<br/>                                                                                                                                                                                                              |
| [**Open, méthode**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open)<br/>                                   | Ouvre la clé de type EK. Vous devez ouvrir la clé de type EK avant de pouvoir récupérer des informations à partir de la clé de type EK, ajouter ou supprimer des certificats ou exporter la clé de type EK.<br/>                                                                                                  |
| [**Méthode RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate)<br/>         | Supprime un certificat de mention lié à la clé de type EK du fournisseur de stockage de clés. Vous pouvez uniquement appeler la méthode [**RemoveCertificate**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-removecertificate) une fois que la méthode [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) a été appelée avec succès.<br/> |



 

 

 




