---
description: En savoir plus sur les attributs XML dans l’infrastructure du schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Attributs XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf76889fdf38c6636b4beb5ba566b18af69e34c
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622975"
---
# <a name="xml-attributes"></a>Attributs XML

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il existe un certain nombre d’attributs XML qui apparaissent dans plusieurs types d’éléments définis dans l’infrastructure du schéma d’impression. Les attributs XML portant le même nom ont généralement la même signification et obéissent aux mêmes règles quel que soit le type d’élément dans lequel elles résident. Par conséquent, les attributs XML sont répertoriés ici par nom et non par leur type d’élément hôte. Les attributs XML définis de manière privée ne sont pas autorisés. Seuls les attributs XML définis ici peuvent être utilisés dans un document PrintCapabilities ou un PrintTicket, puis uniquement dans le contexte défini.

Bien que les parties privées ne soient pas autorisées à introduire de nouvelles définitions dans l’espace de noms d’un autre tiers, elles sont autorisées à utiliser des noms existants à partir d’un autre espace de noms privé, à condition que leur utilisation soit cohérente avec l’utilisation établie par l’autre partie. Par conséquent, une option peut contenir des éléments ScoredProperty définis par plusieurs tiers, chacun résidant dans des espaces de noms différents.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nom de l'attribut</th>
<th>Types de données et valeurs</th>
<th>Objectif</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>QName XML<br/></td>
<td>Cet attribut XML identifie l’instance de l’élément. Elle distingue un élément d’un autre type d’élément. Cet attribut XML est si largement utilisé. il est appelé attribut de nom.<br/></td>
<td>Les restrictions suivantes s’appliquent à l’attribut Name.<br/>
<ul>
<li>L’attribut name doit se présenter sous la forme d’un QName défini par XML valide. Autrement dit, il doit être qualifié par un espace de noms XML valide. Les QNames qui apparaissent en tant que valeurs des attributs de nom doivent être explicitement qualifiés par un espace de noms, même si un espace de noms par défaut est défini. <br/></li>
<li>Le contenu des caractères doit être celui d’un QName défini en XML valide. <br/></li>
<li>Les noms définis en privé doivent être qualifiés avec un espace de noms qui est associé de manière unique au tiers qui a introduit l’attribut Name.<br/></li>
<li>Exigence d’unicité frères : deux éléments frères appartenant au même type d’élément peuvent avoir le même attribut Name. La seule exception concerne les éléments option, où l’attribut Name peut être utilisé pour définir une option. Par conséquent, les éléments d’option à plusieurs frères peuvent avoir le même attribut Name.<br/></li>
<li>Les types d’éléments suivants peuvent contenir des attributs de nom : Property, ScoredProperty, ParameterDef, option et Feature.<br/></li>
<li>les attributs de nom doivent apparaître dans chacun des types d’éléments qui les contiennent, sauf dans le cas de certains éléments d’option de schéma d’impression publics précédemment définis, tels que DocumentNUp.<br/></li>
</ul>
L’exemple suivant montre comment identifier une instance d’option à l’aide d’un attribut’name'. Il s’agit de la méthode correcte pour définir des éléments d’option. Un fournisseur ne doit pas avoir d’options sans nom, sauf s’il est défini publiquement dans le schéma d’impression, par exemple DocumentNUp.<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td>propager <br/></td>
<td>Énumération<br/> Aucune valeur n’est actuellement définie.<br/></td>
<td>L’attribut Propagate n’est pas utilisé dans la version initiale de l’infrastructure du schéma d’impression. Il est documenté ici afin que le code de validation PrintCapabilities ou PrintTicket implémenté pour la version initiale de l’infrastructure du schéma d’impression puisse traiter toutes les versions de schéma suivantes sans erreur.<br/></td>

</tr>
<tr class="odd">
<td>la <br/></td>
<td>Énumération<br/> Valeurs autorisées :<br/>
<ul>
<li>Aucune <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Indique si l’option est disponible pour la sélection ou pour l’utilisation. <br/></td>
<td>Les valeurs autorisées de l’attribut contraction ont les significations suivantes. Notez que ces valeurs sont répertoriées dans l’ordre, de la moins restrictive (aucune) à la plus restrictive (DeviceSettings).<br/> Aucune <br/>
<ul>
<li>L’option n’est pas restreinte. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>L’option est restreinte par les paramètres PrintTicket. Cela implique que la modification de la configuration peut supprimer la contrainte. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>L’option est restreinte par les paramètres de l’administrateur ; l’option ne peut pas être activée par l’utilisateur.<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>L’option est restreinte par les paramètres de l’appareil ou les options de l’appareil physiquement installées ; l’option ne peut pas être activée par l’utilisateur ou par l’administrateur.<br/></li>
</ul>
Lorsque le fournisseur PrintCapabilities signale les valeurs de l’attribut Constrained, la contrainte la plus restrictive trouvée doit être signalée. Par exemple, si une option est restreinte à la fois par un paramètre d’administrateur et un paramètre d’appareil, le fournisseur PrintCapabilities doit signaler DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Cet attribut XML établit un lien entre un URI (Uniform Resource Identifier) d’espace de noms et le préfixe d’espace de noms qui apparaît dans le QName XML. Vous devez établir un lien de ce type vers l’URI d’espace de noms défini pour l’infrastructure du schéma d’impression avant de pouvoir utiliser l’une des balises d’élément, attributs, attributs de nom définis par le Framework, etc. Vous pouvez déclarer cet espace de noms comme étant la valeur par défaut pour éviter de qualifier réellement les balises d’élément avec un préfixe d’espace de noms, bien que tous les autres QNames doivent être qualifiés de manière explicite. L’espace de noms standard doit être défini dans l’élément racine approprié. Observez toutes les règles et conventions XML relatives à l’utilisation de l’attribut xmlns.<br/> L’URI de l’infrastructure du schéma d’impression est http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> L’URI pour les mots clés du schéma d’impression est https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




