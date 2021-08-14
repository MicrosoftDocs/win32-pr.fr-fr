---
description: L’API d’inscription de certificats prend en charge les attributs suivants. Vous pouvez créer un attribut individuel à l’aide de l’interface correspondante identifiée dans chacune des sections suivantes.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Attributs pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8c7945113e764d835a685251adaec9149527b2d8f2d535a5dd24f26a5623bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774412"
---
# <a name="supported-attributes"></a>Attributs pris en charge

L’API d’inscription de certificats prend en charge les attributs suivants. Vous pouvez créer un attribut individuel à l’aide de l’interface correspondante identifiée dans chacune des sections suivantes.

## <a name="clientid"></a>ClientId

L’interface [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) peut être utilisée pour définir un attribut qui contient des informations sur l’ordinateur client qui a envoyé la demande de certificat. Les informations peuvent être utilisées pour les Diagnostics.

**S’applique à :** \#Demande PKCS 10 ou CMC.

**OID :** XCN \_ OID \_ Request \_ client \_ info (1.3.6.1.4.1.311.21.20)

## <a name="extensions"></a>Extensions

L’interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) peut être utilisée pour définir un ensemble d’extensions de certificat X. 509 version 3. Les extensions suivantes sont prises en charge. Pour plus d’informations, consultez la rubrique sur les interfaces d’extension.



| Extension              | Description                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlternativeNames       | Contient une ou plusieurs autres formes de nom de l’émetteur associé au certificat.                                                                                                                                       |
| AuthorityKeyIdentifier | Contient un identificateur de clé unique permettant de différencier plusieurs clés de signature de certificat de l' [*autorité de certification*](/windows/desktop/SecGloss/c-gly) . |
| BasicConstraints       | Indique si le sujet peut agir en tant qu’autorité de certification.                                                                                                                                                                                   |
| CertificatePolicies    | Identifie les stratégies et les informations de qualificateur facultatives associées au certificat.                                                                                                                                      |
| MSApplicationPolicies  | Identifie une ou plusieurs utilisations du certificat. Cette extension est similaire à l’extension champ EnhancedKeyUsage, mais elle est définie par Microsoft.                                                                                           |
| Champ EnhancedKeyUsage       | Identifie une ou plusieurs utilisations de la clé publique contenue dans le certificat. L’extension utilisation améliorée de la clé peut être utilisée en plus ou à la place de l’extension d’utilisation de la clé.                                                  |
| Utilisation               | Identifie des restrictions sur les opérations qui peuvent être effectuées par la clé publique contenue dans le certificat.                                                                                                                  |
| SmimeCapabilities      | Signale les fonctionnalités de déchiffrement d’un destinataire de courrier électronique à l’expéditeur de l’e-mail pour permettre à l’expéditeur de choisir l’algorithme symétrique le plus sécurisé pris en charge par les deux parties.                                                      |
| SubjectKeyIdentifier   | Contient un identificateur de clé unique qui peut être utilisé pour différencier plusieurs clés de signature associées au propriétaire du certificat.                                                                                          |
| Modèle               | Identifie le modèle à utiliser lors de l’émission ou du renouvellement d’un certificat. L’extension contient l’identificateur d’objet (OID) du modèle.                                                                                       |
| TemplateName           | Identifie le modèle à utiliser lors de l’émission ou du renouvellement d’un certificat. L’extension contient le nom du modèle.                                                                                                          |



 

**S’applique à :** \#Demande PKCS 10.

**OID :** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)

## <a name="archivekey"></a>ArchiveKey

L’interface [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) peut être utilisée pour définir un attribut qui contient une clé privée chiffrée soumise à une autorité de certification pour l’archivage.

**S’applique à :** Demande CMC.

**OID :** \_ \_ Attr de la clé archivée XCN OID \_ \_ (1.3.6.1.4.1.311.21.13)

## <a name="archivekeyhash"></a>ArchiveKeyHash

L’interface [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) peut être utilisée pour définir un hachage de la clé privée contenue dans l’attribut **ArchiveKey** .

**S’applique à :** Demande CMC.

**OID :** \_ \_ Hachage de clé chiffrée XCN OID \_ \_ (1.3.6.1.4.1.311.21.21)

## <a name="cspprovider"></a>CspProvider

L’interface [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) peut être utilisée pour définir un attribut qui contient des informations sur le [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) utilisé par le demandeur pour les opérations de chiffrement.

**S’applique à :** \#Demande PKCS 10. Cet attribut est automatiquement créé lorsque vous créez un objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .

**OID :** \_ \_ Fournisseur CSP d’inscription XCN \_ OID \_ (1.3.6.1.4.1.311.13.2.2)

## <a name="osversion"></a>OSVersion

L’interface [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) peut être utilisée pour créer un attribut qui contient des informations de version sur le système d’exploitation client. Les informations peuvent être utilisées par l’autorité de certification pour déterminer le type de traitement à appliquer lors de la création du certificat.

**S’applique à :** \#Demande PKCS 10 ou CMC.

**OID :** \_ \_ Version du système d’exploitation XCN OID \_ (1.3.6.1.4.1.311.13.2.3)

## <a name="renewalcertificate"></a>RenewalCertificate

L’interface [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) peut être utilisée pour créer un attribut qui contient le certificat en cours de renouvellement.

**S’applique à :** \#Demande PKCS 10. Cet attribut est créé automatiquement si vous créez une \# demande PKCS 10 en l’initialisant avec le certificat en cours de renouvellement.

**OID :** \_ \_ Certificat de renouvellement XCN OID \_ (1.3.6.1.4.1.311.13.1)

 

 
