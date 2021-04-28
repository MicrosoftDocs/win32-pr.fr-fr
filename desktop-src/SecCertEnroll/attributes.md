---
description: 'Attributs (API d’inscription de certificats) : des attributs peuvent être ajoutés à une demande de certificat pour fournir à une autorité de certification (CA) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat.'
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributs (API d’inscription de certificats)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118427"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="73f45-103">Attributs (API d’inscription de certificats)</span><span class="sxs-lookup"><span data-stu-id="73f45-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="73f45-104">Des attributs peuvent être ajoutés à une demande de certificat pour fournir à une autorité de certification (CA) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="73f45-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="73f45-105">Chaque attribut est une structure ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) encodée en [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) qui contient un identificateur d’objet (OID) et aucune ou plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="73f45-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="73f45-106">Les attributs sont définis à l’aide d’interfaces incluses avec l’API d’inscription de certificats.</span><span class="sxs-lookup"><span data-stu-id="73f45-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="73f45-107">Les rubriques suivantes traitent des attributs plus en détail :</span><span class="sxs-lookup"><span data-stu-id="73f45-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="73f45-108">Attributs pris en charge</span><span class="sxs-lookup"><span data-stu-id="73f45-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="73f45-109">Architecture des attributs</span><span class="sxs-lookup"><span data-stu-id="73f45-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="73f45-110">\#Attributs PKCS 7</span><span class="sxs-lookup"><span data-stu-id="73f45-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="73f45-111">\#Attributs PKCS 10</span><span class="sxs-lookup"><span data-stu-id="73f45-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="73f45-112">Attributs CMC</span><span class="sxs-lookup"><span data-stu-id="73f45-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
