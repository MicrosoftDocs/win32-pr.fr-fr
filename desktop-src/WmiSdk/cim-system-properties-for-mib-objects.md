---
description: WMI définit un ensemble de propriétés système associées à toutes les classes et instances de classes en plus des propriétés spécifiques à la classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Propriétés système CIM pour les objets MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531710"
---
# <a name="cim-system-properties-for-mib-objects"></a>Propriétés système CIM pour les objets MIB

WMI définit un ensemble de propriétés système associées à toutes les classes et instances de classes en plus des propriétés spécifiques à la classe.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Le fournisseur SNMP utilise les propriétés système CIM suivantes lors du mappage des définitions d’objets MIB aux définitions de classe CIM. Les propriétés obligatoires doivent être présentes pour que le fournisseur SNMP résolve entièrement un objet de groupe. L’impossibilité de définir une propriété obligatoire renvoie une erreur.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>chaîne</strong> Requise<br/> Pour les instances, la classe à laquelle appartient l’objet. Pour les classes, il s’agit du nom de la classe.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>chaîne</strong> Facultatif<br/> Nom de la classe qui est la classe de base la plus fine pour l’objet actuel (pas sa classe parent immédiate).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>UInt32</strong> Requise<br/> Type d'objet. Les valeurs sont les suivantes :<br/> <dl> 1 = classe<br />
2 = instance<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>chaîne</strong> Requise<br/> Espace de noms où se trouve l’objet.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>chaîne</strong> Requise<br/> Chemin d’accès absolu à l’objet.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>UInt32</strong> Requise<br/> Nombre de propriétés non-système définies pour l’objet.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>chaîne</strong> Requise<br/> Chemin d’accès relatif à l’objet.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>chaîne</strong> Requise<br/> Serveur qui fournit l’objet.<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>chaîne</strong> Facultatif<br/> Classe parente immédiate de l’objet.<br/></td>
</tr>
</tbody>
</table>



 

 

 




