---
description: Les attributs sont inclus dans une \# demande de certificat PKCS 10 en les ajoutant à la structure CertificationRequestInfo présentée dans l’exemple de Syntaxe ASN. 1 suivant.
ms.assetid: 5f00f638-9edb-474b-a7e4-f6f7b62c89a4
title: '\#Attributs PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7922f7d308c6956af4c0098ea278a859113af45861ef3d21a20548081e7eee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993289"
---
# <a name="pkcs-10-attributes"></a>\#Attributs PKCS 10

Les attributs sont inclus dans une \# demande de certificat PKCS 10 en les ajoutant à la structure **CertificationRequestInfo** présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations sur la façon dont vous pouvez ajouter des attributs à une demande, consultez la rubrique relative à l' [architecture des attributs](attribute-architecture.md) .

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

L’attribut le plus souvent ajouté à une \# demande PKCS 10 est une collection d’extensions de la version 3 définie par un objet [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) . Comme une \# demande PKCS 10 ne contient pas de champ auquel les extensions peuvent être ajoutées directement, elles doivent être ajoutées en tant qu’attribut. Les attributs **ClientID**, **CspProvider**, **OSVersion** et **RenewalCertificate** peuvent également être ajoutés à une rubrique PKCS).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs pris en charge](supported-attributes.md)
</dt> </dl>

 

 



