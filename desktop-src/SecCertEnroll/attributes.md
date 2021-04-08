---
description: Des attributs peuvent être ajoutés à une demande de certificat pour fournir à une autorité de certification (CA) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753484"
---
# <a name="attributes-certificate-enrollment-api"></a>Attributs (API d’inscription de certificats)

Des attributs peuvent être ajoutés à une demande de certificat pour fournir à une autorité de certification (CA) des informations supplémentaires qu’il peut utiliser lors de la création et de l’émission d’un certificat. Chaque attribut est une structure ASN. 1 ( [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) ) encodée en [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) qui contient un identificateur d’objet (OID) et aucune ou plusieurs valeurs. Les attributs sont définis à l’aide d’interfaces incluses avec l’API d’inscription de certificats. Les rubriques suivantes traitent des attributs plus en détail :

-   [Attributs pris en charge](supported-attributes.md)
-   [Architecture des attributs](attribute-architecture.md)
-   [\#Attributs PKCS 7](pkcs--7-attributes.md)
-   [\#Attributs PKCS 10](pkcs--10-attributes.md)
-   [Attributs CMC](cmc-attributes.md)

 

 
