---
title: Détermination des classes associées à une instance d’objet
description: Chaque objet de Active Directory Domain Services a deux attributs dont les valeurs identifient la hiérarchie des classes d’objets dont l’objet est une instance.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462051"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Détermination des classes associées à une instance d’objet

Chaque objet de Active Directory Domain Services a deux attributs dont les valeurs identifient la hiérarchie des classes d’objets dont l’objet est une instance.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>structuralObjectClass</strong></td>
<td>Identifie les classes structurelles et abstraites dont l’objet est une instance. Par exemple, les valeurs d’un objet utilisateur peuvent être :
<ul>
<li><strong>top</strong></li>
<li><strong>person</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifie les classes incluses dans <strong>structuralObjectClass</strong>, ainsi que toutes les classes auxiliaires qui sont attachées dynamiquement. Par exemple, si une &quot; &quot; classe auxiliaire de véhicule est attachée à un objet utilisateur, les valeurs peuvent être :
<ul>
<li><strong>top</strong></li>
<li><strong>véhicule</strong></li>
<li><strong>person</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

N’oubliez pas qu’aucun de ces attributs n’inclut des classes auxiliaires liées statiquement avec les classes d’objets dont l’objet est une instance. Par exemple, la classe auxiliaire **securityPrincipal** est liée de manière statique à la classe **User** , car elle est incluse dans les valeurs **systemAuxiliaryClass** de l’objet **classSchema** de l’utilisateur. elle n’est pas incluse dans les attributs **objectClass** ou **structuralObjectClass** des instances de la classe User.

 

 




