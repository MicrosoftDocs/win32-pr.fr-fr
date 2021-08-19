---
description: Les ACE spécifiques à l’objet sont prises en charge pour les objets de service d’annuaire (DS). Une entrée du contrôle d’accès spécifique à un objet contient une paire de GUID qui étendent la manière dont l’entrée du contrôle d’accès peut protéger un objet.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE spécifiques à l’objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e322344730f303cd479e4772563aa7b2dc798a154d54828ebd71d92caad111ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118912414"
---
# <a name="object-specific-aces"></a>ACE spécifiques à l’objet

Les [*ACE*](/windows/desktop/SecGloss/a-gly) spécifiques à l’objet sont prises en charge pour les objets de service d’annuaire (DS). Une entrée du contrôle d’accès spécifique à un objet contient une paire de GUID qui étendent la manière dont l’entrée du contrôle d’accès peut protéger un objet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ObjectType</strong></td>
<td>Identifie l’un des éléments suivants :
<ul>
<li>Type d’objet enfant. L’ACE contrôle le droit de créer un type spécifié d’objet enfant. Pour plus d’informations, consultez <a href="controlling-child-object-creation-in-c--.md">contrôle de la création d’objets enfants en C++</a>.</li>
<li>Jeu de propriétés ou propriété. L’ACE contrôle le droit de lire ou d’écrire la propriété ou le jeu de propriétés. Pour plus d’informations, consultez <a href="aces-to-control-access-to-an-object-s-properties.md">ACE pour contrôler l’accès aux propriétés d’un objet</a>.</li>
<li>Un droit étendu. L’ACE contrôle le droit d’exécuter l’opération associée au droit étendu.</li>
<li>Écriture validée. L’ACE contrôle le droit d’effectuer certaines opérations d’écriture. Ces autorisations d’écriture validées, définies et exposées dans l’éditeur ACL, fournissent des autorisations pour les écritures de propriétés validées plutôt que des écritures de bas niveau non contrôlées de toute valeur dans une propriété accordée avec une &quot; autorisation Write Property &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>InheritedObjectType</strong></td>
<td>Indique le type d’objet enfant qui peut hériter de l’entrée du contrôle d’accès. L’héritage est également contrôlé par les indicateurs d’héritage dans le <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, ainsi que par toute protection contre l’héritage placée sur les objets enfants. Pour plus d’informations, consultez <a href="ace-inheritance.md">héritage de l’entrée</a>du contrôle d’accès.</td>
</tr>
</tbody>
</table>



 

Trois types d’ACE spécifiques aux objets sont pris en charge.

> [!Note]  
> Les ACE de l’objet System-Alarm ne sont pas prises en charge actuellement.

 



| Type                      | Description                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE d’accès refusé à l’objet  | Utilisé dans une liste DACL pour refuser à un tiers de confiance l’accès à une propriété ou à une propriété définie sur l’objet, ou pour limiter l’héritage de l’entrée du contrôle d’accès à un type spécifié d’objet enfant. Utilise la structure d' [**\_ ACE d' \_ objet \_ accès refusé**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .         |
| ACE de l’objet Access-allowed | Utilisé dans une liste DACL pour permettre à un tiers de confiance d’accéder à une propriété ou à une propriété définie sur l’objet, ou pour limiter l’héritage de l’entrée du contrôle d’accès à un type spécifié d’objet enfant. Utilise la [**structure \_ \_ \_ ACE access allowed Object**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .      |
| ACE de l’objet audit système   | Utilisé dans une liste SACL pour enregistrer les tentatives d’un tiers de confiance pour accéder à une propriété ou à un jeu de propriétés sur l’objet, ou pour limiter l’héritage de l’entrée du contrôle d’accès à un type spécifié d’objet enfant. Utilise la structure ACE de l' [**\_ \_ objet \_ audit du système**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) . |



 

Toute liste de contrôle d’accès qui contient une entrée du contrôle d’accès spécifique à un objet doit utiliser la révision d’ACL de révision \_ \_ .

 

 
