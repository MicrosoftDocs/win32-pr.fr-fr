---
description: la syntaxe de requête avancée (AQS) est la syntaxe de requête par défaut utilisée par Windows recherche pour interroger l’index et affiner et limiter les paramètres de recherche.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Utilisation de la syntaxe de requête avancée par programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e480866120289605a7465af96d8aaa8dc2beda
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627225"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Utilisation de la syntaxe de requête avancée par programmation

la syntaxe de requête avancée (AQS) est la syntaxe de requête par défaut utilisée par Windows recherche pour interroger l’index et affiner et limiter les paramètres de recherche. AQS est utilisé par les développeurs pour créer des requêtes par programme (et par les utilisateurs pour affiner leurs paramètres de recherche). le AQS canonique a été introduit dans Windows 7 et doit être utilisé dans Windows 7 et versions ultérieures pour générer par programmation des requêtes AQS.

Cette rubrique est organisée comme suit :

-   [À propos de la syntaxe de requête avancée](#about-advanced-query-syntax)
    -   [Exemples](#examples)
    -   [Propriétés](#properties)
-   [Utilisation de mots clés dans les langues locales](#keyword-use-in-local-languages)
-   [syntaxe de requête avancée canonique dans Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [Exemples](#examples)
    -   [Opérateurs de requête](#query-operators)
    -   [Valeurs de requête](#query-values)
-   [Restrictions d’étendue](#scope-restrictions)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-advanced-query-syntax"></a>À propos de la syntaxe de requête avancée

Une requête se compose de requêtes de base connectées avec et, ou, et non, comme indiqué dans l’exemple de syntaxe suivant :

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> AQS ne respecte pas la casse, à l’exception de AND, OR et NOT, qui doit être en majuscules.

 

Si une requête a deux ou plusieurs utilisations de et ou ou, elles sont liées de gauche à droite, qu’il s’agisse de et ou ou. Autrement dit, la requête, « Apple et Poir ou prune », est interprétée comme si elle était écrite comme « (Apple et Poir) ou prune », et la requête, « Apple ou Poir et Plum », sera interprétée comme si elle était écrite comme « (Apple ou Poir) et prune ». Par conséquent, si un document contient le mot Plum, mais ni Apple, ni Poirier, la première requête le retourne, contrairement à la deuxième requête. Par conséquent, nous vous recommandons d’utiliser des parenthèses explicites pour toute requête qui mélange et et ou pour éviter les erreurs ou les interprétations erronées.

Une requête de base recherche les éléments qui répondent à une restriction sur une propriété. La seule partie obligatoire d’une requête de base est la valeur de la restriction ou de la recherche. si vous ne spécifiez pas de propriété, Windows recherche effectue une recherche dans toutes les propriétés. <restr> représente la restriction de recherche.

Les formulaires suivants pour une requête de base sont valides :

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Une propriété est désignée par un mot clé tel que auteur ou taille, ou par un nom de propriété canonique tel que [System. DateModified](../properties/props-system-datemodified.md). Les formulaires valides pour une propriété sont les suivants :

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Un opérateur indique une opération telle que < ou =. Pour obtenir la liste des opérateurs valides, consultez la section opérateurs de requête plus loin dans cette rubrique.

Une restriction de base est une restriction simple sur une propriété qui peut être écrite sans parenthèses :

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Une restriction est une valeur de recherche telle qu’une valeur numérique ou une valeur de chaîne, éventuellement avec un opérateur. Les formulaires valides pour une restriction sont les suivants :

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

si vous ne spécifiez pas d’opérateur, Windows recherche choisit l’opérateur le plus approprié pour votre requête :

-   Pour une propriété de type chaîne, \_ l' \_ opérateur COP Word STARTSWITH $< est supposé.
-   Pour toutes les autres propriétés, l' \_ opérateur COP EQUAL = est supposé.

Pour l’utilisation par programme de AQS, nous vous recommandons de toujours disposer d’un opérateur explicite. Le formulaire valide pour la recherche d’une valeur simple ou d’une plage de valeurs est le suivant :

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

Une valeur simple peut être constituée de l’un des types suivants :

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a>Exemples

Une requête qui recherche un document contenant la phase « dernier trimestre », créée par Theresa ou Lee, et enregistrée dans le dossier MyDocs, combine trois requêtes de base comme suit :

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Les trois requêtes de base sont les suivantes :

-   « dernier trimestre »
-   Auteur : (Theresa ou Lee)
-   dossier : MyDocs

Une requête de base qui utilise la syntaxe canonique est la suivante :

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Propriétés

les propriétés sont référencées par un mot clé, qui peut être un nom de propriété canonique dans Windows 7 et versions ultérieures. AQS dans l’interface utilisateur Windows pouvez utiliser l’étiquette au lieu du nom de propriété canonique, tel que auteur au lieu de [System. author](../properties/props-system-author.md). dans Windows Vista et versions antérieures, il était possible d’utiliser des étiquettes en anglais quelle que soit la langue de l’interface utilisateur. dans Windows 7 et versions ultérieures, Windows recherche reconnaît uniquement les mots clés dans la langue actuelle de l’interface utilisateur par défaut.

### <a name="support-for-custom-properties"></a>Prise en charge des propriétés personnalisées

dans Windows Vista et versions antérieures, les propriétés personnalisées n’étaient pas disponibles dans AQS. dans Windows 7 et versions ultérieures, AQS fonctionne avec des propriétés personnalisées qui sont inscrites auprès du système de propriétés. Pour plus d’informations sur la création de propriétés personnalisées, consultez [système de propriétés](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>Propriétés DateTime dans Windows 8

à partir de Windows 8, les propriétés DateTime (comme [System. DateModified](../properties/props-system-datemodified.md)) prennent en charge le format de date et d’heure canonique spécifié par [ISO-8601](https://www.w3.org/TR/NOTE-datetime), en incluant éventuellement le fuseau horaire UTC.

-   **Windows 8 et versions antérieures, date-heure sans fuseau horaire UTC :** *YYYY* - *MM* - *jjthh*:*MM*:*ss*

    Ce format spécifie une heure locale, quels que soient les paramètres régionaux utilisateur ou système.

-   **Windows 8, date-heure avec fuseau horaire UTC :** *YYYY* - *MM* - *jjthh*:*MM*:*ssTZD*

    Ce format spécifie une heure au fuseau horaire UTC spécifié.

## <a name="keyword-use-in-local-languages"></a>Utilisation de mots clés dans les langues locales

dans Windows 7 et versions ultérieures, les mots clés mnémoniques fonctionnent uniquement dans la langue du système, tels que les mots clés allemands uniquement sur un système d’exploitation allemand et les mots clés en anglais uniquement sur un système d’exploitation anglais. [System. Author](../properties/props-system-author.md) est un mot clé canonique et la valeur mnémonique pour la propriété System. Author est Author, par exemple. l’introduction des mots clés canoniques compense le fait que les mots clés mnémoniques anglais ne sont plus reconnus universellement sur tous les systèmes d’exploitation, quelle que soit la langue, comme c’était le cas dans Windows Vista et versions antérieures.

> [!Note]  
> dans Windows 7 et versions ultérieures, Windows recherche reconnaît les mots clés dans la langue par défaut actuelle uniquement, et non en anglais, sauf si l’anglais est la valeur par défaut actuelle. Nous recommandons que les développeurs utilisent toujours la syntaxe canonique afin que leur application n’ait pas de problèmes de langue avec les mots clés.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>syntaxe de requête avancée canonique dans Windows 7

la syntaxe canonique a été introduite pour les mots clés dans Windows 7. Un exemple de requête avec une propriété canonique est `System.Message.FromAddress:=me@microsoft.com` . lors du codage de requêtes dans des applications qui s’exécutent sur Windows 7 et versions ultérieures, vous devez utiliser la syntaxe canonique pour générer par programmation des requêtes AQS. Si vous n’utilisez pas la syntaxe canonique et que votre application est déployée dans une langue locale ou d’interface utilisateur différente de celle du code de l’application, vos requêtes ne seront pas interprétées correctement.

Les conventions pour la syntaxe de mot clé canonique sont les suivantes :

-   La syntaxe canonique d’une propriété est son nom canonique, tel que `System.Photo.LightSource` . Les noms canoniques ne respectent pas la casse.
-   La syntaxe canonique pour les opérateurs booléens se compose des mots clés AND, OR et NOT, en majuscules.
-   Les opérateurs <, >, =, et ainsi de suite, ne sont pas localisés et font donc également partie de la syntaxe canonique.
-   Si une propriété `P` a des valeurs énumérées ou des plages nommées N ₁ à l’aide de NK, la syntaxe canonique pour la valeur ou la plage *i* est le nom canonique de P, suivi du caractère \# , suivi de N <sub>I</sub>, comme illustré dans l’exemple suivant :
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` , et ainsi de suite.
-   Pour un type sémantique défini T avec des valeurs ou des plages nommées N ₁ à l’aide de NK, la syntaxe canonique pour la valeur ou la plage *i* est le nom canonique de T, suivi du caractère \# , suivi de N <sub>i</sub>, comme illustré dans l’exemple suivant :
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Pour les valeurs littérales telles que des mots ou des expressions, la syntaxe canonique est la même que la syntaxe normale. Voici quelques exemples de requêtes avec des valeurs littérales dans la syntaxe canonique :
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> il n’existe aucune syntaxe canonique pour les nombres dans Windows 7 et versions ultérieures. Étant donné que les formats à virgule flottante varient selon les paramètres régionaux, l’utilisation d’une requête canonique qui implique une constante à virgule flottante n’est pas prise en charge. les constantes entières, en revanche, peuvent être écrites en utilisant uniquement des chiffres (pas de séparateurs pour les milliers) et peuvent être utilisées en toute sécurité dans des requêtes canoniques dans Windows 7 et versions ultérieures.

 

### <a name="examples"></a>Exemples

Le tableau suivant présente quelques exemples de propriétés canoniques et la syntaxe permettant de les utiliser.



| Type de propriété canonique | Exemple                                                                                     | Syntax                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valeur de chaîne               | [System.Author](../properties/props-system-author.md)<br/>    | La valeur de chaîne est recherchée dans la propriété auteur : <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Plage d’énumération          | [System. Priority](../properties/props-system-priority.md)             | La propriété Priority peut avoir une plage de valeurs numériques :<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Booléen                    | [System. IsDeleted](../properties/props-system-isdeleted.md)<br/> | Les valeurs booléennes peuvent être utilisées avec n’importe quelle propriété booléenne :<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True`, et `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numérique                  | [System. Size](../properties/props-system-size.md)<br/>      | Il n’est pas possible d’écrire en toute sécurité une requête canonique qui implique une constante à virgule flottante, car les formats à virgule flottante varient selon les paramètres régionaux. Les entiers doivent être écrits sans séparateurs pour les milliers. Par exemple :<br/>`System.Size:<12345` |



 

Pour plus d’informations sur les propriétés canoniques et le système de propriétés, consultez [Propriétés système](../properties/props.md). Vous pouvez également faire référence aux fichiers d’en-tête publics.

### <a name="query-operators"></a>Opérateurs de requête

Si une propriété, p, a plusieurs valeurs pour un élément, une requête AQS pour p : <restr> retourne l’élément si <restr> a la **valeur true** pour au moins l’une des valeurs. ( <restr> représente une restriction.)

La syntaxe indiquée dans le tableau ci-dessous se compose d’un opérateur, d’un symbole d’opérateur, d’un exemple et d’une description d’exemple. L’opérateur et le symbole peuvent être utilisés dans n’importe quel langage et inclus dans n’importe quelle requête. N’utilisez pas les \_ opérateurs spécifiques à l’application COP implicite ou COP \_ \_ . Certains des opérateurs ont des symboles interchangeables.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Opérateur</th>
<th>Symbole</th>
<th>Exemple</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System. FileExtension : = &quot;.txt&quot;<br/></td>
<td>La valeur est la chaîne &quot; <em>.txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System. Kind : image ≠<br/> System. photo. DateTaken :-[] ¹<br/> System. Kind : &lt; &gt; image<br/> System. Kind : pas d’image<br/> System. Kind :--image<br/></td>
<td>La propriété <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> n’est pas une image.<br/> La propriété <a href="/windows/desktop/properties/props-system-photo-datetaken">System. photo. DateTaken</a> a une valeur.<br/> La propriété <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> n’est pas une image. <br/> La propriété <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> n’est pas une image. <br/> Les opérateurs double NOT appliqués à la même propriété n’annulent pas. Par conséquent, System. Kind :--image est équivalent à System. Kind :-image et System. Kind : pas Picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System. taille : 1 &lt; Ko<br/></td>
<td>Cette valeur est inférieure à 1 <em>Ko</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System. ItemDate : &gt; System. StructuredQueryType. DateTime # Today<br/></td>
<td>Cette valeur est supérieure à la <em>date du jour</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System. Size : &lt; = 1 Ko<br/></td>
<td>Cette valeur est inférieure ou égale à 1 <em>Ko</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System. Size : &gt; = 1 Ko<br/></td>
<td>Cette valeur est supérieure ou égale à 1 <em>Ko</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System. FileName : ~ &lt; &quot; Introduction à C++&quot;<br/></td>
<td>Recherche les éléments dont le nom de fichier commence par les caractères de l' &quot; <em>initiation C++</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System. photo. CameraModel : ~ &gt; non<br/></td>
<td>Recherche les éléments dont la valeur de propriété se termine par les caractères <em>non</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System. Subject. ~ = arrondi <br/> System. Search. AutoSummary : ~ ~ Round<br/></td>
<td>Recherche un message qui a cette chaîne dans l’objet et correspond aux &quot; règles d'<em>arrondi</em> g, &quot; par exemple.<br/> Recherche tous les éléments avec un résumé qui contient les caractères <em>arrondis</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System. Author : ~ ! &quot; Sanjay&quot;<br/></td>
<td>Recherche les auteurs qui n’ont pas de séquence &quot; de caractères<em>Sanjay</em> &quot; .<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System. FileName : ~ &quot; MIC ? osoft W * d&quot;<br/></td>
<td>Recherche les fichiers dont le nom de fichier commence par <em>MIC</em>, suivi d’un caractère, suivi de <em>osoft w</em>, suivi de tous les caractères se terminant par <em>d</em>. <br/> Le point d’interrogation, ?, les caractères et * ne sont pas interprétés littéralement, et fonctionnent comme des caractères génériques de type DOS :<br/>
<ul>
<li>? correspond à un caractère arbitraire.</li>
<li>* correspond à zéro ou plusieurs caractères arbitraires.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System. StructuredQuery. Virtual. from : $ = &quot; Sanjay Jacobs&quot;<br/></td>
<td>pour Windows 7 et versions ultérieures. Recherche l’expression &quot; <em>Sanjay Jacobs</em> &quot; dans toutes les propriétés. Le mot <em>Sanjay</em> doit être suivi du mot <em>Jacobs</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System. Author : $<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>pour Windows 7 et versions ultérieures. Recherche un élément où Author contient un mot commençant par les caractères &quot; <em>San</em> &quot; .<br/> Recherche tout fichier dans lequel le nom de fichier contient un mot commençant par <em>micro</em>, suivi d’un mot commençant par <em>exe</em>.<br/></td>
</tr>
</tbody>
</table>



 

¹ les crochets vides ( \[ \] ) indiquent « aucune valeur ».

Pour les propriétés de type chaîne, l’opération par défaut est COP \_ Word \_ commence \_ par ou COP \_ Word \_ EQUAL.

### <a name="query-values"></a>Valeurs de requête

Le tableau suivant répertorie des exemples utiles de restriction des valeurs de requête.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur/symbole</th>
<th>Exemples</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>auto<br/></td>
<td>Séquence de caractères qui peut être recherchée. La chaîne ne doit pas contenir d’espaces blancs ou de combinaisons de caractères qui font partie de la syntaxe. Cet exemple recherche un mot commençant par <em>auto</em>.<br/></td>
</tr>
<tr class="even">
<td>Chaîne entre guillemets &quot;&quot;</td>
<td>&quot;Conclusions : validez &quot; &quot; l' &quot; &quot; &quot; &quot; équipe Blue Team&quot;<br/></td>
<td>Toute séquence de caractères. La chaîne n’est pas interprétée dans le cadre de la syntaxe.<br/> Les guillemets peuvent être inclus dans une requête s’ils sont doublés. Cet exemple recherche <em>l' &quot; &quot; équipe bleue</em>.<br/></td>
</tr>
<tr class="odd">
<td>Integer</td>
<td>5678<br/></td>
<td>Utilisez uniquement des chiffres pour les entiers. N’utilisez pas de séparateurs pour les milliers.<br/></td>
</tr>
<tr class="even">
<td>Nombre à virgule flottante</td>
<td>5678,1234<br/></td>
<td>Étant donné que les formats à virgule flottante varient selon les paramètres régionaux, une requête canonique ne peut pas utiliser une constante à virgule flottante. L’utilisation de la syntaxe canonique avec des nombres à virgule flottante n’est pas sécurisée pour la localisation. <br/></td>
</tr>
<tr class="odd">
<td>Booléen <strong>true</strong> / <strong>false</strong></td>
<td>System. IsRead : = System. StructuredQueryType. Boolean # true<br/> System. IsEncrypted :-System. StructuredQueryType. Boolean # False<br/></td>
<td>Valeur booléenne <strong>true</strong> .<br/> Valeur booléenne <strong>false</strong> .<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System. Keywords : = []<br/></td>
<td>Les crochets vides indiquent qu’il n’y a aucune valeur. Cet exemple recherche tous les éléments qui n’ont pas été balisés. <br/></td>
</tr>
<tr class="odd">
<td>Dates absolues</td>
<td>System. ItemDate : 1/26/2010<br/> SystemDateModified 10/15/2002 19:00<br/></td>
<td>Recherche les éléments dont la date est le 26 janvier 2010.<br/> Recherche les éléments qui ont été modifiés le 15 octobre 2002 entre les heures 19:00:00 et 19:00:59. <br/>
<blockquote>
[!Note]<br />
Étant donné que les formats de date (comme les formats à virgule flottante) varient selon les paramètres régionaux, l’utilisation de la syntaxe canonique avec des dates absolues n’est pas prise en charge et n’est pas sécurisée pour la localisation.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Dates relatives</td>
<td>System. ItemDate : System. StructuredQueryType. DateTime # Today<br/> System. DateAcquired : System. StructuredQueryType. DateTime # NextMonth<br/> System. message. DateReceived : System. StructuredQueryType. DateTime # LastYear<br/></td>
<td>Recherche des éléments avec la date du jour.<br/> Recherche les éléments dont la date est le mois suivant.<br/> Recherche les éléments dont la date est l’année dernière.<br/>
<blockquote>
[!Note]<br />
En plus de la recherche de dates et de plages de dates spécifiques, AQS reconnaît les valeurs de date relatives (comme <em>aujourd’hui</em>, <em>demain</em>, <em>nextweek</em>, <em>nextMonth</em>) et le jour (par exemple, <em>mardi</em> ou <em>lundi. Mercredi</em>) et mois (<em>février</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System. ItemDate : 11/05/04.. 11/10/04 System. Size : 5 Ko.. 10 Ko<br/></td>
<td>Les doubles périodes indiquent une plage de valeurs. Recherche les éléments dont la date est comprise entre 11/05/04 et 11/10/04 inclus.<br/> Recherche les éléments d’une taille comprise entre 5 et 10KO.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Restrictions d’étendue

Les utilisateurs peuvent limiter l’étendue de leurs recherches à des emplacements de dossiers ou des magasins de données spécifiques. par exemple, si vous utilisez plusieurs comptes de messagerie et que vous souhaitez limiter une requête à microsoft Outlook ou microsoft Outlook Express, vous pouvez utiliser `System.Search.Store:mapi` ou `System.Search.Store:oe` respectivement. Le tableau suivant présente quelques exemples de la manière de limiter une recherche par magasin de données.



| Limiter la recherche par le magasin de données  | Mot clé | Exemple                                     |
|--------------------------------|---------|---------------------------------------------|
| Fichiers                          | fichier    | System. Search. Store : fichier                    |
| Outlook                        | Protocole    | System. Search. Store : MAPI                    |
| Outlook Express                | oe      | System. Search. Store : oe                      |
| Fichiers hors connexion                  | CSC     | System. Search. Store : CSC                     |
| Dossier spécifique sur le lecteur local | dossier  | System. ItemFolderNameDisplay : C : " \\ mondossier" |



 

## <a name="additional-resources"></a>Ressources supplémentaires

-   dans Windows 7 et versions ultérieures, une option de menu contextuel peut être disponible selon qu’une condition AQS est remplie ou non. Pour plus d’informations, consultez « obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée » dans [création de gestionnaires de menus contextuels](../shell/context-menu-handlers.md).
-   Les requêtes AQS peuvent être limitées à des types de fichiers spécifiques, connus sous le nom de types de fichiers. Pour plus d’informations, consultez [types de fichiers et associations](../shell/fa-intro.md). Pour obtenir une documentation de référence sur les propriétés, consultez [System. Kind](../properties/props-system-kind.md)et [System. KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interrogation de l’index programmatiquement](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[utilisation d’approches SQL et AQS pour interroger l’Index](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Interrogation de l’index avec ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Interrogation de l’index avec le protocole search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[interrogation de l’Index avec Windows syntaxe de SQL de recherche](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
