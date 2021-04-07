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
# <a name="cmc-attributes"></a><span data-ttu-id="dbb34-103">Attributs CMC</span><span class="sxs-lookup"><span data-stu-id="dbb34-103">CMC Attributes</span></span>

<span data-ttu-id="dbb34-104">Dans la pratique, la structure d’une demande CMC, indiquée par la syntaxe suivante, est relativement complexe, car elle contient souvent des requêtes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="dbb34-104">In practice, the structure of a CMC request, shown by the following syntax, is relatively complex because it often contains nested requests.</span></span> <span data-ttu-id="dbb34-105">Par exemple, une demande CMC peut contenir zéro ou une demande PKCS \# 10 dans une séquence **TaggedRequest** , et elle peut contenir zéro ou un message PKCS \# 7 dans une séquence **TaggedContentInfo** .</span><span class="sxs-lookup"><span data-stu-id="dbb34-105">For example, a CMC request can contain zero or one PKCS \#10 requests in a **TaggedRequest** sequence, and it can contain zero or one PKCS \#7 messages in a **TaggedContentInfo** sequence.</span></span> <span data-ttu-id="dbb34-106">Chaque \# message PKCS 7 imbriqué peut contenir une demande CMC qui peut, à son tour, contenir plus de demandes.</span><span class="sxs-lookup"><span data-stu-id="dbb34-106">Each nested PKCS \#7 message can contain a CMC request which can, in turn, contain more requests.</span></span> <span data-ttu-id="dbb34-107">Le nombre de niveaux d’imbrication est théoriquement illimité, mais l’autorité de certification (CA) est généralement configurée pour limiter la taille d’une demande.</span><span class="sxs-lookup"><span data-stu-id="dbb34-107">The number of nesting levels is theoretically unlimited, but the certification authority (CA) is typically configured to limit the size of a request.</span></span> <span data-ttu-id="dbb34-108">Les attributs peuvent être appliqués à la demande de niveau supérieur ou aux requêtes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="dbb34-108">Attributes can be applied to the top level request or to the nested requests.</span></span> <span data-ttu-id="dbb34-109">Ce sujet est abordé dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="dbb34-109">This is discussed in the following sections.</span></span>

## <a name="cmcdata-structure"></a><span data-ttu-id="dbb34-110">CMCData, structure</span><span class="sxs-lookup"><span data-stu-id="dbb34-110">CMCData Structure</span></span>

<span data-ttu-id="dbb34-111">Une demande CMC contient des séquences de structures **TaggedAttribute**, **TaggedRequest** et **TaggedContentInfo** ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="dbb34-111">A CMC request contains sequences of **TaggedAttribute**, **TaggedRequest**, and **TaggedContentInfo** ASN.1 structures.</span></span>

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

## <a name="taggedattribute-structure"></a><span data-ttu-id="dbb34-112">TaggedAttribute, structure</span><span class="sxs-lookup"><span data-stu-id="dbb34-112">TaggedAttribute Structure</span></span>

<span data-ttu-id="dbb34-113">Les attributs sont inclus dans une demande de certificat CMC en les ajoutant à la collection **TaggedAttribute** .</span><span class="sxs-lookup"><span data-stu-id="dbb34-113">Attributes are included in a CMC certificate request by adding them to the **TaggedAttribute** collection.</span></span> <span data-ttu-id="dbb34-114">Chaque structure de la collection contient un ID d’entier, un identificateur d’objet (OID) ASN. 1 et un ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="dbb34-114">Each structure in the collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="dbb34-115">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dbb34-115">The possible values can be any of the following.</span></span>

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

## <a name="cmcaddattributes"></a><span data-ttu-id="dbb34-116">CMCAddAttributes</span><span class="sxs-lookup"><span data-stu-id="dbb34-116">CMCAddAttributes</span></span>

<span data-ttu-id="dbb34-117">Si les attributs de cette structure s’appliquent à une requête PKCS 10 imbriquée \# , le champ **certReferences** contient le **BodyPartID** qui identifie la demande.</span><span class="sxs-lookup"><span data-stu-id="dbb34-117">If the attributes in this structure apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="dbb34-118">Si les attributs s’appliquent à une demande CMC imbriquée, le champ **pkiDataReference** contient le **BodyPartID** de la requête.</span><span class="sxs-lookup"><span data-stu-id="dbb34-118">If the attributes apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="dbb34-119">Actuellement, un seul de ces champs peut être différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="dbb34-119">Currently, only one of these fields can be nonzero.</span></span> <span data-ttu-id="dbb34-120">Les attributs qui peuvent être inclus sont répertoriés dans la rubrique [attributs pris en charge](supported-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="dbb34-120">The attributes that can be included are listed in the [Supported Attributes](supported-attributes.md) topic.</span></span>

## <a name="cmcaddextensions"></a><span data-ttu-id="dbb34-121">CmcAddExtensions</span><span class="sxs-lookup"><span data-stu-id="dbb34-121">CmcAddExtensions</span></span>

<span data-ttu-id="dbb34-122">Cette structure peut contenir les extensions X. 509 version 3 et les extensions définies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbb34-122">This structure can contain X.509 version 3 extensions plus extensions defined by Microsoft.</span></span> <span data-ttu-id="dbb34-123">Cet attribut est défini à l’aide de l’interface [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="dbb34-123">This attribute is defined by using the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface.</span></span> <span data-ttu-id="dbb34-124">Si les extensions s’appliquent à une requête PKCS 10 imbriquée \# , le champ **certReferences** contient le **BodyPartID** qui identifie la demande.</span><span class="sxs-lookup"><span data-stu-id="dbb34-124">If the extensions apply to a nested PKCS \#10 request, the **certReferences** field will contain the **BodyPartID** that identifies the request.</span></span> <span data-ttu-id="dbb34-125">Si les extensions s’appliquent à une demande CMC imbriquée, le champ **pkiDataReference** contient le **BodyPartID** de la demande.</span><span class="sxs-lookup"><span data-stu-id="dbb34-125">If the extensions apply to a nested CMC request, the **pkiDataReference** field will contain the **BodyPartID** of the request.</span></span> <span data-ttu-id="dbb34-126">Actuellement, un seul de ces champs peut être différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="dbb34-126">Currently, only one of these fields can be nonzero.</span></span>

## <a name="sendernonce"></a><span data-ttu-id="dbb34-127">SenderNonce</span><span class="sxs-lookup"><span data-stu-id="dbb34-127">SenderNonce</span></span>

<span data-ttu-id="dbb34-128">Une valeur à usage unique est une donnée binaire aléatoire ou Pseudo-aléatoire qui peut être incluse dans une transaction de demande de certificat et de réponse pour garantir que la réponse ou la demande n’est pas une répétition d’un message précédent.</span><span class="sxs-lookup"><span data-stu-id="dbb34-128">A nonce is random or pseudo-random binary data that can be included in a certificate request and response transaction to help ensure that the response or request is not a repeat of a previous message.</span></span> <span data-ttu-id="dbb34-129">Pour plus d’informations, consultez la propriété [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) .</span><span class="sxs-lookup"><span data-stu-id="dbb34-129">For more information, see the [**SenderNonce**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_sendernonce) property.</span></span>

## <a name="transactid"></a><span data-ttu-id="dbb34-130">TransactID</span><span class="sxs-lookup"><span data-stu-id="dbb34-130">TransactID</span></span>

<span data-ttu-id="dbb34-131">Une demande de certificat d’aller-retour et une transaction de réponse peuvent être suivies à l’aide d’un identificateur.</span><span class="sxs-lookup"><span data-stu-id="dbb34-131">A round trip certificate request and response transaction can be tracked using an identifier.</span></span> <span data-ttu-id="dbb34-132">Le client génère un ID de transaction et le conserve jusqu’à ce que le certificat ou l’autorité d’inscription réponde avec un message qui termine la transaction.</span><span class="sxs-lookup"><span data-stu-id="dbb34-132">The client generates a transaction ID and retains it until the certificate or registration authority responds with a message that completes the transaction.</span></span> <span data-ttu-id="dbb34-133">La réponse comprend l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="dbb34-133">The response includes the identifier.</span></span> <span data-ttu-id="dbb34-134">Pour plus d’informations, consultez la propriété [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) .</span><span class="sxs-lookup"><span data-stu-id="dbb34-134">For more information, see the [**TransactionId**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_transactionid) property.</span></span>

## <a name="reginfo"></a><span data-ttu-id="dbb34-135">RegInfo</span><span class="sxs-lookup"><span data-stu-id="dbb34-135">RegInfo</span></span>

<span data-ttu-id="dbb34-136">Cet attribut peut être utilisé pour contenir les informations d’inscription que le client choisit de placer dans la demande CMC.</span><span class="sxs-lookup"><span data-stu-id="dbb34-136">This attribute can be used to contain any registration information that the client chooses to put into the CMC request.</span></span> <span data-ttu-id="dbb34-137">La valeur de l’attribut est une chaîne qui contient des paires nom-valeur concaténées.</span><span class="sxs-lookup"><span data-stu-id="dbb34-137">The attribute value is string that contains concatenated name-value pairs.</span></span> <span data-ttu-id="dbb34-138">Pour plus d’informations, consultez la propriété [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) .</span><span class="sxs-lookup"><span data-stu-id="dbb34-138">For more information, see the [**NameValuePairs**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_namevaluepairs) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbb34-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dbb34-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbb34-140">Attributs pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbb34-140">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



