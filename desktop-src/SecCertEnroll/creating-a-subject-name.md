---
description: Vous pouvez utiliser l’interface IX500DistinguishedName pour créer un nom d’objet à partir d’une chaîne de nom unique.
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: Création d’un nom d’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a7350268c4b7fe5f0d6bde0630bfa7556bc8dd6085e11261456299b725dd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670209"
---
# <a name="creating-a-subject-name"></a>Création d’un nom d’objet

Vous pouvez utiliser l’interface [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) pour créer un nom d’objet à partir d’une chaîne de nom unique. La chaîne se compose de noms uniques relatifs concaténés (RDN). Les clés RDN suivantes sont prises en charge par l’API d’inscription de certificats.

| Clé                               | OID                                             | Description                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | nom du pays de l' \_ OID XCN \_ \_<br/>              | Contient un code de pays ou de région ISO 3166 à deux lettres.<br/>                                  |
| CN<br/>                     | \_ \_ nom commun de l’OID XCN \_<br/>               | Contient un nom commun.<br/>                                                                 |
| E<br/> MESSAGERIE<br/>     | XCN \_ OID \_ RSA \_ emailaddr<br/>             | Contient une adresse de messagerie.<br/>                                                              |
| DC<br/>                     | \_composant de \_ domaine XCN OID \_<br/>          | Contient une partie d’un nom DNS (Domain Name System).<br/>                                   |
| G<br/> GivenName<br/> | nom d’XCN \_ OID \_ donné \_<br/>                | Contient la partie du nom d’une personne qui n’est pas un nom de famille.<br/>                             |
| I<br/>                      | \_initiales OID \_ XCN<br/>                   | Contient les initiales d’une personne.<br/>                                                           |
| L<br/>                      | nom de la localité de l' \_ OID XCN \_ \_<br/>             | Contient le nom de la localité qui identifie une ville, un pays ou une autre région géographique.<br/> |
| O<br/>                      | nom de l' \_ organisation XCN OID \_ \_<br/>         | Contient le nom d’une organisation.<br/>                                                   |
| OU<br/>                     | nom de l' \_ \_ unité d’organisation XCN OID \_ \_<br/> | Contient le nom d’une sous-division d’unité au sein d’une organisation.<br/>                         |
| S<br/> ST<br/>        | \_ \_ état \_ ou nom de la \_ province \_ XCN OID<br/>  | Contient le nom complet d’un État ou d’une province.<br/>                                          |
| STREET<br/>                 | \_ \_ adresse postale de l’OID XCN \_<br/>            | Contient l’adresse physique.<br/>                                                          |
| SN<br/>                     | XCN \_ OID sur le \_ \_ nom<br/>                  | Contient le nom de famille d’une personne.<br/>                                                   |
| T<br/> TITLE<br/>     | titre de l' \_ OID XCN \_<br/>                      | Contient le titre d’une personne de l’organisation.<br/>                                     |



 

Lorsque vous initialisez un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , vous pouvez identifier le format du nom unique en spécifiant une valeur à partir du type d’énumération [**l x500nameflags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) . Par exemple, supposons que le nom unique du sujet se compose des noms de RDN suivants :<dl> CN = administrateur  
CN = utilisateurs  
DC = jdomcsc  
DC = nttest  
DC = Microsoft  
DC = com  
</dl>

Si vous concaténez ces RDN dans la chaîne de nom unique délimitée par des virgules suivante, vous pouvez spécifier la valeur de l’indicateur de la **virgule de nom de \_ certificat XCN \_ \_ Str \_ \_** lors de l’initialisation d’un objet [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) .

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage d’un nom de sujet](encoding-a-subject-name.md)
</dt> <dt>

[Noms de sujets](subject-names.md)
</dt> </dl>

 

 




