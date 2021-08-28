---
description: le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble des American National Standards Institute langage SQL (ANSI SQL) &\# 8212 ; avec des modifications sémantiques mineures. Le tableau suivant répertorie les mots clés WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL for WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e2c80473874390851e81a5f2acebcd6d7e1497
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626755"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL for WMI)

le Langage de requêtes WMI (WQL) (WQL) est un sous-ensemble des American National Standards Institute langage SQL (ANSI SQL) avec des modifications sémantiques mineures. Le tableau suivant répertorie les mots clés WQL.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Mot clé WQL</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>Combine deux expressions booléennes et retourne la <strong>valeur true</strong> lorsque les deux expressions ont la <strong>valeur true</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOCIATEURS DE</a></td>
<td>Récupère toutes les instances associées à une instance source.<br/> Utilisez cette instruction avec les requêtes de schéma et les requêtes de données.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Fait référence à la classe de l’objet dans une requête.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Spécifie la classe qui contient les propriétés listées dans une instruction SELECT. Windows WMI (Management Instrumentation) ne prend en charge les requêtes de données que d’une seule classe à la fois.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">GROUP, clause</a></td>
<td>Permet à WMI de générer une notification pour représenter un groupe d’événements.<br/> Utilisez cette clause avec des requêtes d’événements.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtre les événements reçus pendant l’intervalle de regroupement spécifié dans la <a href="within-clause.md">clause within</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Opérateur de comparaison utilisé avec NOT et <strong>null</strong>. La syntaxe de cette instruction est la suivante :<br/> IS [NOT] <strong>null</strong><br/> (où NOT est facultatif)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Opérateur qui applique une requête aux sous-classes d’une classe spécifiée. Pour plus d’informations, consultez <a href="isa-operator-for-event-queries.md">opérateur ISA pour les requêtes d’événements</a>, <a href="isa-operator-for-data-queries.md">opérateur ISA pour les requêtes de données</a>et <a href="isa-operator-for-schema-queries.md">opérateur ISA pour les requêtes de schéma</a>.<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Utilisé dans les <a href="references-of-statement.md">références</a> et les <a href="associators-of-statement.md">associateurs de</a> requêtes pour s’assurer que les instances résultantes sont remplies uniquement avec les clés des instances, ce qui réduit la surcharge de l’appel.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Opérateur qui détermine si une chaîne de caractères donnée correspond à un modèle spécifié.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Opérateur de comparaison qui utilise dans une requête WQL SELECT, par exemple :<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indique qu’un objet n’a pas de valeur assignée explicitement. <strong>Null</strong> n’est pas équivalent à zéro (0) ou vide.<br/></td>
</tr>
<tr class="odd">
<td>OR<br/></td>
<td>Combine deux conditions.<br/> Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, les opérateurs ou sont évalués après les opérateurs et.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">RÉFÉRENCES DE</a></td>
<td>Récupère toutes les instances d’association qui font référence à une instance source spécifique. Utilisez cette instruction avec les requêtes de schéma et de données. Les <a href="references-of-statement.md">références de</a> l’instruction sont similaires aux <a href="associators-of-statement.md">ASSOCIATORS de</a> l’instruction. Toutefois, il ne récupère pas les instances de point de terminaison ; Il récupère les instances d’association.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Spécifie les propriétés utilisées dans une requête.<br/> Pour plus d’informations, consultez <a href="select-statement-for-data-queries.md">instruction SELECT pour les requêtes de données</a>, <a href="select-statement-for-event-queries.md">instruction SELECT pour les requêtes d’événement</a>ou <a href="select-statement-for-schema-queries.md">instruction SELECT pour les requêtes de schéma</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Opérateur booléen qui prend la valeur-1 (moins un).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Réduit l’étendue d’une requête de données, d’événement ou de schéma.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Spécifie un intervalle d’interrogation ou de regroupement.<br/> Utilisez cette clause avec des requêtes d’événements.<br/></td>
</tr>
<tr class="odd">
<td>false<br/></td>
<td>Opérateur booléen qui prend la valeur 0 (zéro).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> L’utilisation d’un mot clé WQL comme nom d’objet peut entraîner une requête qui ne peut pas être analysée même lorsque la requête est compilée sans erreur.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérateurs WQL](wql-operators.md)
</dt> <dt>

[Formats de date pris en charge par WQL](wql-supported-date-formats.md)
</dt> <dt>

[Formats d’heure pris en charge par WQL](wql-supported-time-formats.md)
</dt> </dl>

 

 




