---
description: Les extensions sont incluses dans une demande CMC en les ajoutant à la structure TaggedAttributes présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations, consultez la rubrique attributs.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Extensions CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d29873bc43f7a7229b363a7b09cdf03a23127cc5d5e0e738036c6005a6cc7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901842"
---
# <a name="cmc-extensions"></a>Extensions CMC

Les extensions sont incluses dans une demande CMC en les ajoutant à la structure **TaggedAttributes** présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations, consultez la rubrique [attributs](attributes.md) .

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

Chaque structure de la collection **TaggedAttributes** contient un ID d’entier, un identificateur d’objet (OID) ASN. 1 et un ensemble de valeurs. Les extensions sont incorporées dans une requête en ajoutant une structure **CmcAddExtensions** au champ **valeurs** . La syntaxe de la structure ASN. 1 est présentée dans l’exemple suivant. L’identificateur d’objet est **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).

``` syntax
CmcAddExtensions ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   extensions              Extensions
}

Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
   extnId              EncodedObjectID,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTETSTRING
}
```

La procédure suivante explique comment utiliser l’API d’inscription de certificats pour ajouter des extensions à une demande de certificat CMC.

**Pour utiliser l’API d’inscription de certificats afin d’ajouter des extensions à une demande de certificat CMC**

1.  Créez une extension en utilisant l’une des interfaces disponibles qui dérivent de l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) ou utilisez l’objet **IX509Extension** directement pour créer des extensions personnalisées.
2.  Appelez la propriété [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) sur l’objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) pour récupérer une collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
3.  Ajoutez les extensions créées à l’étape 1 à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .
4.  Appelez [**inscrire**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) pour effectuer automatiquement les actions suivantes :
    -   Récupérez un objet [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) à partir de l’objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .
    -   Créez et initialisez un objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) à l’aide de la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) Récupérée à l’étape 2.
    -   Créez une collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) et ajoutez-y l’objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .
    -   Utilisez la collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) pour initialiser un objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .
    -   Ajoutez l’objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à la collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs](attributes.md)
</dt> <dt>

[Architecture des attributs](attribute-architecture.md)
</dt> <dt>

[Attributs CMC](cmc-attributes.md)
</dt> <dt>

[Extensions](extensions.md)
</dt> </dl>

 

 



