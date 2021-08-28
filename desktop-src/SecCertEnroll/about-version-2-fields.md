---
description: Un certificat X.509 version 2 contient les champs de base définis dans la version 1, ainsi que les champs supplémentaires suivants.
ms.assetid: 533d43d7-0c49-4461-8ba8-368c103feb4f
title: Champs de la version 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7aed470acfbc3c9a648de46f89a72dc3de361e61eed39cdce4aebbf28e133f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903425"
---
# <a name="version-2-fields"></a>Champs de la version 2

Un certificat X.509 version 2 contient les champs de base définis dans la version 1, ainsi que les champs supplémentaires suivants.

## <a name="issuer-unique-identifier"></a>Identificateur unique de l’émetteur

Contient une valeur unique pouvant être utilisée pour rendre le nom X.500 de l’autorité de certification non ambigu lorsqu’il est réutilisé par différentes entités au fil du temps.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
issuerUniqueIdentifier ::= [1] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="subject-unique-identifier"></a>Identificateur unique du sujet

Contient une valeur unique pouvant être utilisée pour rendre le nom X.500 du sujet du certificat non ambigu lorsqu’il est réutilisé par différentes entités au fil du temps.

``` syntax
---------------------------------------------------------------------
-- Issuer Unique identifier
---------------------------------------------------------------------
subjectUniqueIdentifier ::= [2] IMPLICIT UniqueIdentifier OPTIONAL

UniqueIdentifier ::= BITSTRING
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Champs de base](about-basic-fields.md)
</dt> <dt>

[Extensions de la version 3](about-version-3-extensions.md)
</dt> <dt>

[Certificats de clé publique X. 509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 



