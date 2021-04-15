---
description: Le chiffrement à clé publique s’appuie sur une paire de clés publique et privée pour chiffrer et déchiffrer le contenu.
ms.assetid: a85ec2bc-a413-41a6-b3d2-5fa81a9e7bb6
title: Certificats de clé publique X. 509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acd602e9b47cb7825f6d75df0fb74399b914db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562484"
---
# <a name="x509-public-key-certificates"></a>Certificats de clé publique X. 509

Le chiffrement à clé publique s’appuie sur une paire de clés publique et privée pour chiffrer et déchiffrer le contenu. Les clés sont liées mathématiquement, et le contenu chiffré à l’aide de l’une des clés ne peut être déchiffré qu’à l’aide de l’autre. La clé privée est gardée secrète. La clé publique est généralement incorporée dans un certificat binaire, et le certificat est publié dans une base de données accessible par tous les utilisateurs autorisés.

La norme de l’infrastructure à clé publique (PKI) X. 509 identifie la configuration requise pour les certificats de clé publique robustes. Un certificat est une structure de données signée qui lie une clé publique à une personne, un ordinateur ou une organisation. Les certificats sont émis par des [*autorités de certification*](/windows/desktop/SecGloss/c-gly) (ca). Toutes les personnes qui sont parties à sécuriser les communications qui utilisent une clé publique s’appuient sur l’autorité de certification pour vérifier correctement les identités des personnes, des systèmes ou des entités auxquels elle émet des certificats. Le niveau de vérification dépend généralement du niveau de sécurité requis pour la transaction. Si l’autorité de certification peut vérifier correctement l’identité du demandeur, il signe (chiffre), encode et émet le certificat.

Un certificat est une structure de données signée qui lie une clé publique à une entité. La syntaxe ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) pour le certificat [*X. 509*](/windows/desktop/SecGloss/x-gly) version 3 est présentée dans l’exemple suivant.

``` syntax
-- X.509 signed certificate 

SignedContent ::= SEQUENCE 
{
  certificate         CertificateToBeSigned,
  algorithm           Object Identifier,
  signature           BITSTRING
}
 
-- X.509 certificate to be signed

CertificateToBeSigned ::= SEQUENCE 
{
  version                 [0] CertificateVersion DEFAULT v1,
  serialNumber            CertificateSerialNumber,
  signature               AlgorithmIdentifier,
  issuer                  Name
  validity                Validity,
  subject                 Name
  subjectPublicKeyInfo    SubjectPublicKeyInfo,
  issuerUniqueIdentifier  [1] IMPLICIT UniqueIdentifier OPTIONAL,
  subjectUniqueIdentifier [2] IMPLICIT UniqueIdentifier OPTIONAL,
  extensions              [3] Extensions OPTIONAL
}
```

Depuis sa création dans 1998, trois versions de la norme de certificat de clé publique X. 509 ont évolué. Comme indiqué dans l’illustration suivante, chaque version successive de la structure de données a conservé les champs qui existaient dans les versions précédentes et en a ajouté davantage.

![certificats x. 509 versions 1, 2 et 3](images/x509certificateversions.png)

Les rubriques suivantes décrivent les champs disponibles plus en détail :

-   [Champs de base](about-basic-fields.md)
-   [Champs de la version 2](about-version-2-fields.md)
-   [Extensions de la version 3](about-version-3-extensions.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Infrastructure à clé publique (PKI)](public-key-infrastructure.md)
</dt> </dl>

 

 
