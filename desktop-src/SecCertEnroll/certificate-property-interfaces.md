---
description: Les interfaces suivantes peuvent être utilisées pour créer une propriété de certificat.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Interfaces de propriété de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3d0ab8d9f8e9bb73d47b7e112dfa0ff6fb11f70031c64405b660ee5096dd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902605"
---
# <a name="certificate-property-interfaces"></a>Interfaces de propriété de certificat

Les interfaces suivantes peuvent être utilisées pour créer une propriété de certificat.



| Interface                                                                          | Description                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Gérer une collection d’objets [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) .                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Associe une propriété externe à un certificat.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Représente une propriété de certificat qui détermine si un certificat a été archivé.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Représente un hachage SHA-1 d’une clé privée chiffrée soumise à une autorité de certification pour l’archivage.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Représente une propriété de certificat qui identifie un modèle qui a été configuré pour activer l’inscription automatique du certificat.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Représente une propriété de certificat qui identifie si un certificat a été sauvegardé et, le cas échéant, la date et l’heure de son enregistrement.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Vous permet de spécifier et de récupérer une chaîne qui contient des informations descriptives pour un certificat.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Représente une propriété de certificat qui contient les informations de certificat et d’autorité de certification créées lorsque le client appelle la méthode d' [**inscription**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) sur l’interface [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) . |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Représente une propriété de certificat externe qui contient des informations sur un serveur de stratégie d’inscription de certificats (CEP) et un serveur d’inscription de certificats (EC).                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Vous permet de spécifier et de récupérer une chaîne qui contient le nom complet d’un certificat.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Représente une propriété de certificat qui contient des informations sur une clé privée.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Représente une propriété de certificat qui contient un hachage SHA-1 du nouveau certificat créé lors du renouvellement d’un certificat existant.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Représente une propriété de certificat qui contient le nom DNS de l’ordinateur sur lequel la demande a été créée.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Représente une propriété de certificat qui contient le nom DNS de l’ordinateur sur lequel la demande a été créée.                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



