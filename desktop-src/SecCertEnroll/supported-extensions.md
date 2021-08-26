---
description: Vous pouvez utiliser l’interface IX509Extension pour définir une extension arbitraire.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensions prises en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0362bc289e8f0631520a7d9d56ff4bed1af2c698c721db703b27b0ecee5a1629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101108"
---
# <a name="supported-extensions"></a>Extensions prises en charge

Vous pouvez utiliser l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) pour définir une extension arbitraire. L’API d’inscription de certificats fournit également des interfaces dérivées de **IX509Extension** pour vous permettre de créer facilement les extensions les plus courantes. La liste suivante identifie les extensions communes prises en charge par les autorités de certification Microsoft, ainsi que les identificateurs d’objets et les interfaces que vous pouvez utiliser pour les créer.

## <a name="alternativenames"></a>AlternativeNames

L’extension de noms alternatifs peut être utilisée pour définir une ou plusieurs autres formes de nom pour l’objet de la demande de certificat. Parmi les autres formes, citons : adresses de messagerie, noms DNS, adresses IP et URI.

**Interface :** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)

**OID :** XCN \_ OID \_ Subject \_ Alt \_ nom2 (2.5.29.17)

## <a name="authorityinformationaccess"></a>AuthorityInformationAccess

L’extension d’accès aux informations de l’autorité identifie l’accès aux informations et aux services de l’autorité de certification. La valeur d’extension contient une séquence d’URI.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** XCN \_ OID \_ Authority \_ info \_ Access (1.3.6.1.5.5.7.1.1)

## <a name="authoritykeyidentifier"></a>AuthorityKeyIdentifier

L’extension de l’identificateur de clé de l’autorité permet l’identification de la clé publique de l’autorité de certification qui correspond à la clé privée de l’autorité de certification qui a signé un certificat émis. il est utilisé par le logiciel de création de chemin d’accès de certificat sur un serveur de Windows pour rechercher le certificat d’autorité de certification. Lorsqu’une autorité de certification émet un certificat, la valeur de l’extension est égale à l’extension **extension SubjectKeyIdentifier** dans le certificat de signature de l’autorité de certification. La valeur est généralement un hachage SHA-1 de la clé publique.

**Interface :** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)

**OID :** \_ \_ Clé de l’autorité XCN OID \_ \_ identificateur2 (2.5.29.35)

## <a name="basicconstraints"></a>BasicConstraints

L’extension de contraintes de base peut être utilisée pour déterminer si l’entité peut être utilisée en tant qu’autorité de certification (CA) et, le cas échéant, le nombre d’autorités de certification secondaires qui peuvent exister sous celle-ci dans la chaîne de certificats.

**Interface :** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)

**OID :** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)

## <a name="certificatepolicies"></a>CertificatePolicies

L’extension des stratégies de certificat peut être utilisée pour identifier les stratégies sous lesquelles le certificat a été émis, ainsi que les objectifs qui peuvent être utilisés. Celles-ci sont identifiées par une collection d’identificateurs d’objet (OID). Les stratégies sont personnalisées pour les besoins d’une organisation.

**Interface :** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)

**OID :** \_ \_ Stratégies de certificat XCN OID \_ (2.5.29.32)

## <a name="crldistributionpoints"></a>CrlDistributionPoints

L’extension des points de distribution de la liste de révocation de certificats (CRL) contient l’URI de la liste de révocation de certificats de base.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** \_ \_ Points de distribution de liste de révocation de certificats XCN OID \_ \_ (2.5.29.31)

## <a name="enhancedkeyusage"></a>Champ EnhancedKeyUsage

L’extension utilisation améliorée de la clé peut être utilisée pour définir une ou plusieurs utilisations de la clé publique contenue dans le certificat.

**Interface :** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)

**OID :** \_ \_ Utilisation améliorée de la clé XCN OID \_ \_ (2.5.29.37)

## <a name="freshestcrl"></a>FreshestCRL

L’extension de la liste de révocation de certificats la plus récente contient l’URI de la liste CRL Delta. La même syntaxe ASN. 1 est utilisée pour cette extension et l’extension **CrlDistributionPoints** .

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** XCN \_ OID le plus \_ actualisé \_ (2.5.29.46)

## <a name="keyusage"></a>Utilisation

L’extension d’utilisation de la clé peut être utilisée pour définir des restrictions sur les opérations qui peuvent être effectuées par la clé publique contenue dans le certificat. Par exemple, vous pouvez spécifier que la clé publique doit être utilisée uniquement pour créer une signature numérique, signer une liste de révocation de certificats (CRL) ou chiffrer une autre clé.

**Interface :** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)

**OID :** \_ \_ Utilisation de la clé XCN OID \_ (2.5.29.15)

## <a name="msapplicationpolicies"></a>MSApplicationPolicies

L’extension des stratégies d’application Microsoft peut être utilisée par une application pour filtrer les certificats sur la base de l’utilisation autorisée. Les utilisations autorisées sont identifiées par des OID. Cette extension est similaire à l’extension **champ EnhancedKeyUsage** , mais avec des sémantiques plus strictes appliquées à l’autorité de certification parente. L’extension est spécifique à Microsoft.

**Interface :** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)

**OID :** XCN \_ OID \_ application \_ CERT \_ Policies (1.3.6.1.4.1.311.21.10)

## <a name="nameconstraints"></a>NameConstraints

L’extension de contraintes de nom est utilisée pour identifier l’espace de noms dans lequel tous les noms d’objet des certificats dans une hiérarchie de certificats doivent être localisés. L’extension n’est utilisée que dans un certificat d’autorité de certification.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** \_ \_ Contraintes de nom XCN OID \_ (2.5.29.30)

## <a name="policyconstraints"></a>PolicyConstraints

L’extension de contraintes de stratégie est ajoutée aux certificats de l’autorité de certification pour limiter la validation du chemin d’accès en interdisant le mappage de la stratégie ou en exigeant que chaque certificat de la hiérarchie contienne un identificateur de stratégie acceptable.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** \_ \_ Contraintes de la stratégie OID XCN \_ (2.5.29.36)

## <a name="policymappings"></a>PolicyMappings

L’extension mappages de stratégie permet d’identifier les stratégies d’une autorité de certification secondaire qui correspondent aux stratégies de l’autorité de certification émettrice. La valeur d’extension contient une séquence d’autorités de certification émettrices et des mappages de stratégie d’autorité de certification subordonnée représentés par des identificateurs d’objets.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** \_ \_ Mappages de la stratégie OID XCN \_ (2.5.29.33)

## <a name="privatekeyusageperiod"></a>PrivateKeyUsagePeriod

L’extension de période d’utilisation de la clé privée est utilisée pour spécifier une période de validité différente pour la clé privée que pour le certificat auquel la clé est associée.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** \_Période d' \_ utilisation de XCN OID PRIVATEKEY \_ \_ (2.5.29.16)

## <a name="smimecapabilities"></a>SmimeCapabilities

L’extension des fonctionnalités S/MIME (Secure/Multipurpose Internet Mail Extensions) peut être utilisée pour signaler les fonctionnalités de déchiffrement d’un destinataire de courrier électronique à l’expéditeur du message électronique, afin que l’expéditeur puisse choisir l’algorithme de chiffrement le plus sécurisé pris en charge par les deux parties. La valeur d’extension contient une collection d’OID d’algorithme de chiffrement symétrique et une force de chiffrement facultative pour chacun.

**Interface :** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)

**OID :** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)

## <a name="subjectdirectoryattributes"></a>SubjectDirectoryAttributes

L’extension des attributs du répertoire du sujet peut être utilisée pour transmettre des attributs d’identification tels que la nationalité de l’objet du certificat. La valeur de l’extension est une séquence de paires OID-valeur.

**Interface :** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)

**OID :** XCN \_ OID \_ Subject \_ dir \_ ATTRS (2.5.29.9)

## <a name="subjectkeyidentifier"></a>SubjectKeyIdentifier

L’extension de l’identificateur de clé du sujet peut être utilisée pour différencier plusieurs clés publiques détenues par l’objet du certificat. La valeur de l’extension est généralement un hachage SHA-1 de la clé.

**Interface :** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)

**OID :** \_ \_ Identificateur de clé du sujet de l’OID XCN \_ \_ (2.5.29.14)

## <a name="template"></a>Modèle

L’extension de modèle peut être utilisée pour identifier le modèle de version 2 à utiliser lors de l’émission ou du renouvellement d’un certificat. La valeur de l’extension contient l’OID du modèle et les informations de version facultatives. L’extension est spécifique à Microsoft.

**Interface :** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)

**OID :** \_ \_ Modèle de certificat XCN OID \_ (1.3.6.1.4.1.311.21.7)

## <a name="templatename"></a>TemplateName

L’extension de nom de modèle peut être utilisée pour identifier le modèle de version 1 à utiliser lors de l’émission ou du renouvellement d’un certificat. La valeur de l’extension contient le nom du modèle. L’extension est spécifique à Microsoft.

**Interface :** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)

**OID :** XCN \_ OID \_ inscrire \_ le type \_ extension (1.3.6.1.4.1.311.20.2)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Extensions](extensions.md)
</dt> </dl>

 

 



