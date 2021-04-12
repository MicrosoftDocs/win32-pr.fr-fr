---
description: Les extensions sont incluses dans une demande CMC en les ajoutant à la structure TaggedAttributes présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations, consultez la rubrique attributs.
ms.assetid: 3aa9175b-f889-4d5d-8eb2-a8a42f9fe750
title: Extensions CMC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b104af2b28470627ea593321627ae5e5076b1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203995"
---
# <a name="cmc-extensions"></a><span data-ttu-id="a3283-104">Extensions CMC</span><span class="sxs-lookup"><span data-stu-id="a3283-104">CMC Extensions</span></span>

<span data-ttu-id="a3283-105">Les extensions sont incluses dans une demande CMC en les ajoutant à la structure **TaggedAttributes** présentée dans l’exemple de Syntaxe ASN. 1 suivant.</span><span class="sxs-lookup"><span data-stu-id="a3283-105">Extensions are included in a CMC request by adding them to the **TaggedAttributes** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="a3283-106">Pour plus d’informations, consultez la rubrique [attributs](attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="a3283-106">For more information, see the [Attributes](attributes.md) topic.</span></span>

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

<span data-ttu-id="a3283-107">Chaque structure de la collection **TaggedAttributes** contient un ID d’entier, un identificateur d’objet (OID) ASN. 1 et un ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="a3283-107">Each structure in the **TaggedAttributes** collection contains an integer ID, an ASN.1 object identifier (OID), and a set of values.</span></span> <span data-ttu-id="a3283-108">Les extensions sont incorporées dans une requête en ajoutant une structure **CmcAddExtensions** au champ **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="a3283-108">Extensions are incorporated into a request by adding a **CmcAddExtensions** structure to the **values** field.</span></span> <span data-ttu-id="a3283-109">La syntaxe de la structure ASN. 1 est présentée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="a3283-109">The ASN.1 structure syntax is shown in the following example.</span></span> <span data-ttu-id="a3283-110">L’identificateur d’objet est **XCN \_ OID \_ CMC \_ Add \_ Extensions** (1.3.6.1.5.5.7.7.8).</span><span class="sxs-lookup"><span data-stu-id="a3283-110">The object identifier is **XCN\_OID\_CMC\_ADD\_EXTENSIONS** (1.3.6.1.5.5.7.7.8).</span></span>

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

<span data-ttu-id="a3283-111">La procédure suivante explique comment utiliser l’API d’inscription de certificats pour ajouter des extensions à une demande de certificat CMC.</span><span class="sxs-lookup"><span data-stu-id="a3283-111">The following procedure discusses how to use the Certificate Enrollment API to add extensions to a CMC certificate request.</span></span>

<span data-ttu-id="a3283-112">**Pour utiliser l’API d’inscription de certificats afin d’ajouter des extensions à une demande de certificat CMC**</span><span class="sxs-lookup"><span data-stu-id="a3283-112">**To use the Certificate Enrollment API to add extensions to a CMC certificate request**</span></span>

1.  <span data-ttu-id="a3283-113">Créez une extension en utilisant l’une des interfaces disponibles qui dérivent de l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) ou utilisez l’objet **IX509Extension** directement pour créer des extensions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="a3283-113">Create an extension by using any of the available interfaces that derive from the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface or use the **IX509Extension** object directly to create custom extensions.</span></span>
2.  <span data-ttu-id="a3283-114">Appelez la propriété [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) sur l’objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) pour récupérer une collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="a3283-114">Call the [**X509Extensions**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_x509extensions) property on the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object to retrieve an [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
3.  <span data-ttu-id="a3283-115">Ajoutez les extensions créées à l’étape 1 à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) .</span><span class="sxs-lookup"><span data-stu-id="a3283-115">Add the extensions created in step 1 to the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection.</span></span>
4.  <span data-ttu-id="a3283-116">Appelez [**inscrire**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) pour effectuer automatiquement les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3283-116">Call [**Enroll**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) to automatically perform the following actions:</span></span>
    -   <span data-ttu-id="a3283-117">Récupérez un objet [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) à partir de l’objet [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) .</span><span class="sxs-lookup"><span data-stu-id="a3283-117">Retrieve an [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) object from the [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) object.</span></span>
    -   <span data-ttu-id="a3283-118">Créez et initialisez un objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) à l’aide de la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) Récupérée à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="a3283-118">Create and initialize an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object by using the [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) collection retrieved in step 2.</span></span>
    -   <span data-ttu-id="a3283-119">Créez une collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) et ajoutez-y l’objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="a3283-119">Create an [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection and add the [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object to it.</span></span>
    -   <span data-ttu-id="a3283-120">Utilisez la collection [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) pour initialiser un objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="a3283-120">Use the [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes) collection to initialize an [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object.</span></span>
    -   <span data-ttu-id="a3283-121">Ajoutez l’objet [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) à la collection [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) .</span><span class="sxs-lookup"><span data-stu-id="a3283-121">Add the [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) object to the [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes) collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3283-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3283-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3283-123">Attributs</span><span class="sxs-lookup"><span data-stu-id="a3283-123">Attributes</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="a3283-124">Architecture des attributs</span><span class="sxs-lookup"><span data-stu-id="a3283-124">Attribute Architecture</span></span>](attribute-architecture.md)
</dt> <dt>

[<span data-ttu-id="a3283-125">Attributs CMC</span><span class="sxs-lookup"><span data-stu-id="a3283-125">CMC Attributes</span></span>](cmc-attributes.md)
</dt> <dt>

[<span data-ttu-id="a3283-126">Extensions</span><span class="sxs-lookup"><span data-stu-id="a3283-126">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



