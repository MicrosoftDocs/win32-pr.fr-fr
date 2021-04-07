---
description: Dans la pratique, la structure d’une demande CMC, indiquée par la syntaxe suivante, est relativement complexe, car elle contient souvent des requêtes imbriquées.
ms.assetid: faeee338-bce4-4b35-9be9-72a6568fa259
title: Attributs CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6778575a9359ad5b8764528fb0351b68efc1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758073"
---
# <a name="cmc-attributes"></a>Attributs CMC

Dans la pratique, la structure d’une demande CMC, indiquée par la syntaxe suivante, est relativement complexe, car elle contient souvent des requêtes imbriquées. Par exemple, une demande CMC peut contenir zéro ou une demande PKCS \# 10 dans une séquence **TaggedRequest** , et elle peut contenir zéro ou un message PKCS \# 7 dans une séquence **TaggedContentInfo** . Chaque \# message PKCS 7 imbriqué peut contenir une demande CMC qui peut, à son tour, contenir plus de demandes. Le nombre de niveaux d’imbrication est théoriquement illimité, mais l’autorité de certification (CA) est généralement configurée pour limiter la taille d’une demande. Les attributs peuvent être appliqués à la demande de niveau supérieur ou aux requêtes imbriquées. Ce sujet est abordé dans les sections suivantes.

## <a name="cmcdata-structure"></a>CMCData, structure

Une demande CMC contient des séquences de structures **TaggedAttribute**, **TaggedRequest** et **TaggedContentInfo** ASN. 1.

``` syntax
CmcData ::= SEQUENCE 
{
   controlSequence         ControlSequence,
   reqSequence             ReqSequence,
   cmsSequence             CmsSequence,
   otherMsgSequence        OtherMsgSequence
}


ControlSequence  ::=    SEQUENCE OF TaggedAttribute
ReqSequence      ::=    SEQUENCE OF TaggedRequest
CmsSequence      ::=    SEQUENCE OF TaggedContentInfo

TaggedAttribute ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   type                    EncodedObjectID,
   values                  AttributeSetValue
}

TaggedRequest ::= CHOICE 
{
   tcr                     [0] IMPLICIT TaggedCertificationRequest
}

TaggedContentInfo ::= SEQUENCE 
{
   bodyPartID              BodyPartID,
   contentInfo             ANY
}

BodyPartID ::= INTEGER (0..4294967295)
EncodedObjectID ::= OBJECT IDENTIFIER
AttributeSetValue ::= SET OF ANY
```

## <a name="taggedattribute-structure"></a>TaggedAttribute, structure

Les attributs sont inclus dans une demande de certificat CMC en les ajoutant à la collection **TaggedAttribute** . Chaque structure de la collection contient un ID d’entier, un identificateur d’objet (OID) ASN. 1 et un ensemble de valeurs. Les valeurs possibles sont les suivantes :

``` syntax
CmcAddAttributes ::= SEQUENCE 
{
   pkiDataReference        BodyPartID,
   certReferences          BodyPartIDSequence,
   attributes              Attributes
}

Attributes ::= SET OF Attribute
Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}

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

SenderNonce ::= OCTET STRING

TransactID ::= OCTET STRING

RegInfo ::= OCTET STRING
```

## <a name="cmcaddattributes"></a>CMCAddAttributes

Si les attributs de cette structure s’appliquent à une requête PKCS 10 imbriquée \# , le champ **certReferences** contient le **BodyPartID** qui identifie la demande. Si les attributs s’appliquent à une demande CMC imbriquée, le champ **pkiDataReference** contient le **BodyPartID** de la requête. Actuellement, un seul de ces champs peut être différent de zéro. Les attributs qui peuvent être inclus sont répertoriés dans la rubrique [attributs pris en charge](supported-attributes.md) .

## <a name="cmcaddextensions"></a>CmcAddExtensions

Cette structure peut contenir les extensions X. 509 version 3 et les extensions définies par Microsoft. Cet attribut est défini à l’aide de l’interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Si les extensions s’appliquent à une requête PKCS 10 imbriquée \# , le champ **certReferences** contient le **BodyPartID** qui identifie la demande. Si les extensions s’appliquent à une demande CMC imbriquée, le champ **pkiDataReference** contient le **BodyPartID** de la demande. Actuellement, un seul de ces champs peut être différent de zéro.

## <a name="sendernonce"></a>SenderNonce

Une valeur à usage unique est une donnée binaire aléatoire ou Pseudo-aléatoire qui peut être incluse dans une transaction de demande de certificat et de réponse pour garantir que la réponse ou la demande n’est pas une répétition d’un message précédent. Pour plus d’informations, consultez la propriété [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .

## <a name="transactid"></a>TransactID

Une demande de certificat d’aller-retour et une transaction de réponse peuvent être suivies à l’aide d’un identificateur. Le client génère un ID de transaction et le conserve jusqu’à ce que le certificat ou l’autorité d’inscription réponde avec un message qui termine la transaction. La réponse comprend l’identificateur. Pour plus d’informations, consultez la propriété [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .

## <a name="reginfo"></a>RegInfo

Cet attribut peut être utilisé pour contenir les informations d’inscription que le client choisit de placer dans la demande CMC. La valeur de l’attribut est une chaîne qui contient des paires nom-valeur concaténées. Pour plus d’informations, consultez la propriété [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs pris en charge](supported-attributes.md)
</dt> </dl>

 

 



