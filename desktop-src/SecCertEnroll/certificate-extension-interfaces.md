---
description: Les interfaces suivantes peuvent être utilisées pour créer des extensions de certificat.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Interfaces d’extension de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526332"
---
# <a name="certificate-extension-interfaces"></a>Interfaces d’extension de certificat

Les interfaces suivantes peuvent être utilisées pour créer des extensions de certificat.



| Interface                                                                            | Description                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Représente une instance d’une extension **AlternativeNames** .                                                                                   |
| [**IAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Gère une collection d’objets [**IAlternativeName**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) .                                                                  |
| [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Spécifie une stratégie de certificat qui identifie l’objectif pour lequel le certificat peut être utilisé.                                              |
| [**ICertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Gère une collection d’objets [**ICertificatePolicy**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) .                                                              |
| [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Représente un qualificateur qui peut être associé à une stratégie de certificat.                                                                       |
| [**IPolicyQualifiers**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Gère une collection d’objets [**IPolicyQualifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) .                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Définit une extension pour une demande de certificat.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Spécifie une ou plusieurs autres formes de nom pour l’objet d’un certificat.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Représente une extension **authorityKeyIdentifier** .                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Spécifie si l’objet du certificat est une autorité de certification et, le cas échéant, la profondeur de la chaîne de l’autorité de certification secondaire. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Représente une collection de termes d’informations de stratégie.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Représente une collection d’identificateurs d’objets qui indiquent comment un certificat peut être utilisé par une application.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Représente une collection d’identificateurs d’objets qui identifient les utilisations prévues de la clé publique contenue dans un certificat.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Représente des restrictions sur les opérations qui peuvent être effectuées par la clé publique contenue dans le certificat.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Gère une collection d’objets [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Représente une collection qui signale les fonctionnalités de déchiffrement d’un destinataire de courrier électronique à un expéditeur de courrier électronique.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Représente une extension **extension SubjectKeyIdentifier** utilisée pour identifier un certificat de signature.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Représente une extension **CertificateTemplate** qui contient un modèle de version 2.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Représente une extension **CertificateTemplateName** qui contient un modèle de version 1.                                                         |
| [**ISmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Gère une collection d’objets [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) .                                                                  |
| [**ISmimeCapability**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Représente une extension **SMIMECapabilities** qui identifie les fonctionnalités de déchiffrement d’un destinataire de courrier électronique.                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CertEnroll, interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



