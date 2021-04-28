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
# <a name="attributes-certificate-enrollment-api"></a>Attributs (API d’inscription de certificats)

Des attributs peuvent être ajoutés à une demande de certificat pour fournir à une autorité de certification (CA) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat. Chaque attribut est une structure ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) encodée en [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) qui contient un identificateur d’objet (OID) et aucune ou plusieurs valeurs. Les attributs sont définis à l’aide d’interfaces incluses avec l’API d’inscription de certificats. Les rubriques suivantes traitent des attributs plus en détail :

-   [Attributs pris en charge](supported-attributes.md)
-   [Architecture des attributs](attribute-architecture.md)
-   [\#Attributs PKCS 7](pkcs--7-attributes.md)
-   [\#Attributs PKCS 10](pkcs--10-attributes.md)
-   [Attributs CMC](cmc-attributes.md)

 

 
