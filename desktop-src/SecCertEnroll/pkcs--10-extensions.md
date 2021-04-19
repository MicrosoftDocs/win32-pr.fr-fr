---
description: Les extensions sont incluses dans une \# demande de certificat PKCS 10 en les ajoutant au champ attributs de la structure CertificationRequestInfo présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations, consultez la rubrique attributs.
ms.assetid: 26fa8476-a0ad-4114-a1e7-ed3d4fc9d30e
title: '\#Extensions PKCS 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba71f0a24f50503fd92b3b9670b787dea3b9ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531197"
---
# <a name="pkcs-10-extensions"></a>\#Extensions PKCS 10

Les extensions sont incluses dans une \# demande de certificat PKCS 10 en les ajoutant au champ **attributs** de la structure **CertificationRequestInfo** présentée dans l’exemple de Syntaxe ASN. 1 suivant. Pour plus d’informations, consultez la rubrique [attributs](attributes.md) .

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

La procédure suivante explique comment utiliser l’API d’inscription de certificats pour ajouter des extensions à une demande de \# certificat PKCS 10 :

1.  Récupérez une collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) en appelant la propriété [**X509Extension**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_x509extensions) sur l’objet [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
2.  Créez une extension en utilisant l’une des interfaces disponibles qui dérivent de l’interface [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .
3.  Ajoutez les extensions créées à l’étape 2 à la collection [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions) Récupérée à l’étape 1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs](attributes.md)
</dt> <dt>

[Architecture des attributs](attribute-architecture.md)
</dt> <dt>

[\#Attributs PKCS 10](pkcs--10-attributes.md)
</dt> <dt>

[Extensions](extensions.md)
</dt> </dl>

 

 



