---
description: Un certificat X.509 version 3 contient les champs définis dans les versions 1 et 2 et ajoute des extensions de certificat. La syntaxe ASN. 1 des extensions de certificat est présentée dans l’exemple suivant.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Extensions de la version 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202837"
---
# <a name="version-3-extensions"></a>Extensions de la version 3

Un certificat X.509 version 3 contient les champs définis dans les versions 1 et 2 et ajoute des extensions de certificat. La syntaxe ASN. 1 des extensions de certificat est présentée dans l’exemple suivant.

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

Les extensions standard version 3 et leurs identificateurs d’objet (OID) sont répertoriés dans le tableau suivant. Microsoft les prend en charge et comprend des extensions personnalisées supplémentaires. Pour plus d’informations, consultez [Extensions](extensions.md).

| Extension                                         | Description                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificateur de clé de l’autorité (2.5.29.19)<br/>    | Identifie la clé publique de l’autorité de certification qui correspond à la clé privée de l’autorité de certification utilisée pour signer le certificat.                                                                              |
| Contraintes de base (2.5.29.35)<br/>           | Indique si l’entité peut être utilisée en tant qu’autorité de certification et, le cas échéant, le nombre d’autorités de certification secondaires pouvant exister en dessous dans la chaîne de certificats.                                                           |
| Stratégies de certificat (2.5.29.32)<br/>        | Indique les stratégies sous lesquelles le certificat a été émis et les fins auxquelles il peut être utilisé.                                                                                            |
| Points de distribution de liste de révocation de certificats (2.5.29.31)<br/>     | Contient l’URI de la [*liste de révocation de certificats*](/windows/desktop/SecGloss/c-gly) de base.                                  |
| Utilisation améliorée de la clé (2.5.29.46)<br/>          | Indique la façon dont la clé publique contenue dans le certificat peut être utilisée.                                                                                                                   |
| Autre nom de l’émetteur (2.5.29.8)<br/>      | Indique un ou plusieurs autres noms pour l’émetteur de la demande de certificat.                                                                                                                  |
| Utilisation de la clé (2.5.29.15)<br/>                   | Indique des restrictions sur les opérations pouvant être effectuées par la clé publique contenue dans le certificat.                                                                                           |
| Contraintes de nom (2.5.29.30)<br/>            | Indique l’espace de noms dans lequel tous les noms de sujets d’une hiérarchie de certificats doivent se trouver. L’extension n’est utilisée que dans un certificat d’autorité de certification.                                                       |
| Contraintes de stratégie (2.5.29.36)<br/>          | Contraint la validation du chemin d’accès en interdisant le mappage de stratégie ou en exigeant que tous les certificats de la hiérarchie contiennent un identificateur de stratégie acceptable. L’extension n’est utilisée que dans un certificat d’autorité de certification. |
| Mappages de stratégie (2.5.29.33)<br/>             | Indique les stratégies dans une autorité de certification secondaire qui correspondent aux stratégies dans l’autorité de certification émettrice.                                                                                                                |
| Période d’utilisation de la clé privée (2.5.29.16)<br/>    | Indique une durée de validité pour la clé privée qui est différente de celle du certificat auquel la clé privée est associée.                                                                             |
| Autre nom de l’objet (2.5.29.17)<br/>    | Indique une ou plusieurs autres formes de noms pour le sujet de la demande de certificat. Parmi les autres formes, citons : adresses de messagerie, noms DNS, adresses IP et URI.                           |
| Attributs du répertoire du sujet (2.5.29.9)<br/> | Véhicule des attributs d’identification tels que la nationalité du sujet du certificat. La valeur de l’extension est une séquence de paires OID-valeur.                                                              |
| Identificateur de la clé du sujet (2.5.29.14)<br/>      | Fait la distinction entre plusieurs clés publiques détenues par le sujet du certificat. La valeur de l’extension est généralement un hachage SHA-1 de la clé.                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Champs de base](about-basic-fields.md)
</dt> <dt>

[Champs de la version 2](about-version-2-fields.md)
</dt> <dt>

[Certificats de clé publique X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

