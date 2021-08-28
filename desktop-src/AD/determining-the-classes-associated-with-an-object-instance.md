---
title: Détermination des classes associées à une instance d’objet
description: Chaque objet de Active Directory Domain Services a deux attributs dont les valeurs identifient la hiérarchie des classes d’objets dont l’objet est une instance.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af65b5e1abf7f0bc68ae115cb409d2cdb556e08
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471495"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Détermination des classes associées à une instance d’objet

Chaque objet de Active Directory Domain Services a deux attributs dont les valeurs identifient la hiérarchie des classes d’objets dont l’objet est une instance.




| Attribut | Description | 
|-----------|-------------|
| <strong>structuralObjectClass</strong> | Identifie les classes structurelles et abstraites dont l’objet est une instance. Par exemple, les valeurs d’un objet utilisateur peuvent être :<ul><li><strong>top</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 
| <strong>objectClass</strong> | Identifie les classes incluses dans <strong>structuralObjectClass</strong>, ainsi que toutes les classes auxiliaires qui sont attachées dynamiquement. Par exemple, si une classe auxiliaire « Vehicle » est attachée à un objet utilisateur, les valeurs peuvent être :<ul><li><strong>top</strong></li><li><strong>véhicule</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 




 

N’oubliez pas qu’aucun de ces attributs n’inclut des classes auxiliaires liées statiquement avec les classes d’objets dont l’objet est une instance. Par exemple, la classe auxiliaire **securityPrincipal** est liée de manière statique à la classe **User** , car elle est incluse dans les valeurs **systemAuxiliaryClass** de l’objet **classSchema** de l’utilisateur. elle n’est pas incluse dans les attributs **objectClass** ou **structuralObjectClass** des instances de la classe User.

 

 




