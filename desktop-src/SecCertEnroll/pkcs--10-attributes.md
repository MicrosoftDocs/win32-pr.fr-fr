---
description: Les attributs sont inclus dans une \# demande de certificat PKCS 10 en les ajoutant à la structure CertificationRequestInfo présentée dans l’exemple de Syntaxe ASN. 1 suivant.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#Attributs PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c69260fa09b99c4d91fa1f8bcdafeb4b0da285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321050"
---
# <a name="pkcs-10-attributes"></a><span data-ttu-id="4372f-103">\#Attributs PKCS 10</span><span class="sxs-lookup"><span data-stu-id="4372f-103">PKCS \#10 Attributes</span></span>

<span data-ttu-id="4372f-104">Les attributs sont inclus dans une \# demande de certificat PKCS 10 en les ajoutant à la structure **CertificationRequestInfo** présentée dans l’exemple de Syntaxe ASN. 1 suivant.</span><span class="sxs-lookup"><span data-stu-id="4372f-104">Attributes are included in a PKCS \#10 certificate request by adding them to the **CertificationRequestInfo** structure shown in the following ASN.1 syntax example.</span></span> <span data-ttu-id="4372f-105">Pour plus d’informations sur la façon dont vous pouvez ajouter des attributs à une demande, consultez la rubrique relative à l' [architecture des attributs](attribute-architecture.md) .</span><span class="sxs-lookup"><span data-stu-id="4372f-105">For more information about how you can add attributes to a request, see the [Attribute Architecture](attribute-architecture.md) topic.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 ANY,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type       EncodedObjectID,
   values     AttributeSetValue
}
```

<span data-ttu-id="4372f-106">L’attribut le plus souvent ajouté à une \# demande PKCS 10 est une collection d’extensions de la version 3 définie par un objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) .</span><span class="sxs-lookup"><span data-stu-id="4372f-106">The attribute most commonly added to a PKCS \#10 request is a collection of version 3 extensions defined by an [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) object.</span></span> <span data-ttu-id="4372f-107">Comme une \# demande PKCS 10 ne contient pas de champ auquel les extensions peuvent être ajoutées directement, elles doivent être ajoutées en tant qu’attribut.</span><span class="sxs-lookup"><span data-stu-id="4372f-107">Because a PKCS \#10 request does not contain a field to which the extensions can be directly added, they must be added as an attribute.</span></span> <span data-ttu-id="4372f-108">Les attributs **ClientID**, **CspProvider**, **OSVersion** et **RenewalCertificate** peuvent également être ajoutés à une rubrique PKCS).</span><span class="sxs-lookup"><span data-stu-id="4372f-108">The **ClientId**, **CspProvider**, **OSVersion**, and **RenewalCertificate** attributes can also be added to a PKCS ) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4372f-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4372f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4372f-110">Attributs pris en charge</span><span class="sxs-lookup"><span data-stu-id="4372f-110">Supported Attributes</span></span>](supported-attributes.md)
</dt> </dl>

 

 



