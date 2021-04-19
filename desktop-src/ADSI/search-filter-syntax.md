---
title: Syntaxe de filtre de recherche
description: Les filtres de recherche vous permettent de définir des critères de recherche et de fournir des recherches plus efficaces et efficaces.
ms.assetid: 3ce4709c-5ef7-4713-8fb7-b46ab284339f
ms.tgt_platform: multiple
keywords:
- Syntaxe de filtre de recherche ADSI
- requêtes, syntaxe de filtre de recherche
ms.topic: article
ms.date: 09/25/2020
ms.openlocfilehash: 28875bd49a3d1df7418c37706e58852066bbe08a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106521782"
---
# <a name="search-filter-syntax"></a>Syntaxe de filtre de recherche

Les filtres de recherche vous permettent de définir des critères de recherche et de fournir des recherches plus efficaces et efficaces.

ADSI prend en charge les filtres de recherche LDAP tels que définis dans RFC2254. Ces filtres de recherche sont représentés par des chaînes Unicode. Le tableau suivant répertorie quelques exemples de filtres de recherche LDAP.



| Filtre de recherche                                                               | Description                                                |
|-----------------------------------------------------------------------------|------------------------------------------------------------|
| "(objectClass = \* )"                                                          | Tous les objets.                                               |
| "(& (objectCategory = person) (objectClass = user) ( ! ( CN = Andy)))»                  | Tous les objets utilisateur, mais « Andy ».                               |
| « (SN = SM \* ) »                                                                 | Tous les objets dont le nom commence par « SM ».          |
| « (& (objectCategory = person) (objectClass = contact) ( \| (SN = Smith) (SN = Johnson))) » | Tous les contacts dont le nom est égal à « Smith » ou « Johnson ». |



 

Ces filtres de recherche utilisent l’un des formats suivants.


```C++
<filter>=(<attribute><operator><value>)
```



ou


```C++
(<operator><filter1><filter2>)
```



Les filtres de recherche ADSI sont utilisés de deux manières. Ils constituent une partie du dialecte LDAP pour l’envoi de requêtes via le fournisseur OLE DB. Ils sont également utilisés avec l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

## <a name="operators"></a>Opérateurs

Le tableau suivant répertorie les opérateurs de filtre de recherche fréquemment utilisés.



| Opérateur logique | Description                                |
|------------------|--------------------------------------------|
| =                | Égal à                                   |
| ~=               | Approximativement égal à                     |
| <=            | Vue lexicographique inférieur ou égal à    |
| >=            | Vue lexicographique supérieur ou égal à |
| &                | AND                                        |
| \|               | OR                                         |
| !                | NOT                                        |



 

En plus des opérateurs ci-dessus, LDAP définit deux identificateurs d’objet de règle de correspondance (OID) qui peuvent être utilisés pour effectuer des comparaisons au niveau du bit des valeurs numériques. Les règles de correspondance ont la syntaxe suivante.


```C++
<attribute name>:<matching rule OID>:=<value>
```



« &lt; nom &gt; d’attribut » est le **lDAPDisplayName** de l’attribut, « &lt; la règle OID &gt; » est l’OID de la règle de correspondance et « &lt; valeur &gt; » est la valeur à utiliser pour la comparaison. N’oubliez pas que les espaces ne peuvent pas être utilisés dans cette chaîne. « &lt; value &gt; » doit être un nombre décimal ; il ne peut pas s’agir d’un nombre hexadécimal ou d’un nom de constante, tel que la **\_ sécurité du type de groupe ADS \_ \_ \_ activée**. Pour plus d’informations sur les attributs de Active Directory disponibles, consultez [tous les attributs](/windows/desktop/ADSchema/attributes-all).

Le tableau suivant répertorie les OID de règles de correspondance implémentés par LDAP.



| OID de règle de correspondance       | Identificateur de chaîne (à partir de Ntldap. h)   | Description                                                                                                                                                                                   |
|-------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.2.840.113556.1.4.803  | **\_ \_ \_ bit de règle de correspondance LDAP \_ et**  | Une correspondance est trouvée uniquement si tous les bits de l’attribut correspondent à la valeur. Cette règle est équivalente à un opérateur **de bits and** .                                                                  |
| 1.2.840.113556.1.4.804  | **\_ \_ \_ bit de règle de correspondance LDAP \_ ou**   | Une correspondance est trouvée si des bits de l’attribut correspondent à la valeur. Cette règle est équivalente à un opérateur **de bits or** .                                                                        |
| 1.2.840.113556.1.4.1941 | **\_ \_ règle de correspondance LDAP dans la \_ \_ chaîne** | Cette règle est limitée aux filtres qui s’appliquent au DN. Il s’agit d’un opérateur de correspondance « étendu » spécial qui parcourt la chaîne de ascendance dans des objets jusqu’à la racine jusqu’à ce qu’il trouve une correspondance. |



 

L’exemple suivant de chaîne de requête recherche les objets de groupe pour lesquels l’indicateur de **sécurité de type de groupe ADS est \_ \_ \_ \_ activé** est défini. Sachez que la valeur décimale de la **\_ sécurité de type de groupe ADS \_ \_ \_ activée** (0x80000000 = 2147483648) est utilisée pour la valeur de comparaison.


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=2147483648))
```



La **\_ \_ règle de correspondance LDAP de la \_ \_ chaîne** est un OID de règle de correspondance conçu pour fournir une méthode permettant de rechercher le ascendance d’un objet. De nombreuses applications qui utilisent Active Directory et AD LDS fonctionnent généralement avec des données hiérarchiques, classées par relations parent-enfant. Auparavant, les applications effectuaient une expansion de groupe transitives pour déterminer l’appartenance à un groupe, qui utilisait trop de bande passante réseau. les applications devaient effectuer plusieurs allers-retours pour déterminer si un objet a baissé « dans la chaîne » si un lien est parcouru jusqu’à la fin.

Un exemple d’une telle requête est conçu pour vérifier si un utilisateur « utilisateur1 » est membre du groupe « Group1 ». Vous devez définir la base sur le nom unique de l’utilisateur `(cn=user1, cn=users, dc=x)` et l’étendue sur `base` , et utiliser la requête suivante.


```C++
(memberof:1.2.840.113556.1.4.1941:=cn=Group1,OU=groupsOU,DC=x)
```



De même, pour rechercher tous les groupes dont est membre « utilisateur1 », définissez la base sur le nom unique du conteneur de groupes ; par exemple `(OU=groupsOU, dc=x)` , et l’étendue à `subtree` , et utilisez le filtre suivant.


```C++
(member:1.2.840.113556.1.4.1941:=cn=user1,cn=users,DC=x)
```



Notez que lors de l’utilisation **\_ d’une \_ règle de correspondance LDAP dans la \_ \_ chaîne**, l’étendue n’est pas limitée ; il peut s’agir de `base` , `one-level` ou `subtree` . Certaines de ces requêtes sur les sous-arborescences peuvent être plus gourmandes en processeur, telles que la recherche de liens avec un grand éventail de ventilation ; autrement dit, répertorie tous les groupes dont un utilisateur est membre. Les recherches inefficaces consignent les messages du journal des événements appropriés, comme avec tout autre type de requête.

## <a name="wildcards"></a>Caractères génériques

Vous pouvez également ajouter des caractères génériques et des conditions à un filtre de recherche LDAP. Les exemples suivants montrent des sous-chaînes qui peuvent être utilisées pour effectuer des recherches dans l’annuaire.

Récupérer toutes les entrées :


```C++
(objectClass=*)
```



Récupérez les entrées contenant « Bob » quelque part dans le nom commun :


```C++
(cn=*bob*)
```



Obtenir les entrées avec un nom commun supérieur ou égal à « Bob » :


```C++
(cn>='bob')
```



Obtient tous les utilisateurs avec un attribut de messagerie :


```C++
(&(objectClass=user)(email=*))
```



Obtenir toutes les entrées d’utilisateur avec un attribut de messagerie et un nom égal à « Smith » :


```C++
(&(sn=smith)(objectClass=user)(email=*))
```



Obtient toutes les entrées d’utilisateur avec un nom commun qui commence par « Andy », « Steve » ou « Margaret » :


```C++
(&(objectClass=user)(| (cn=andy*)(cn=steve*)(cn=margaret*)))
```



Récupération de toutes les entrées sans attribut de messagerie :


```C++
(!(email=*))
```



La définition formelle du filtre de recherche est la suivante (à partir de la [RFC 2254](https://tools.ietf.org/html/rfc2254)) :


```C++
<filter> ::= '(' <filtercomp> ')'
<filtercomp> ::= <and> | <or> | <not> | <item>
<and> ::= '&' <filterlist>
<or> ::= '|' <filterlist>
<not> ::= '!' <filter>
<filterlist> ::= <filter> | <filter> <filterlist>
<item>::= <simple> | <present> | <substring>
<simple> ::= <attr> <filtertype> <value><filtertype> ::= <equal> | <approx> | <ge> | <le>
<equal> ::= '='
<approx> ::= '~='
<ge> ::= '>='
<le> ::= '<='
<present> ::= <attr> '=*'
<substring> ::= <attr> '=' <initial> <any> <final>
<initial> ::= NULL | <value><any> ::= '*' <starval>
<starval> ::= NULL | <value>'*' <starval>
<final> ::= NULL | <value>
```



Le jeton &lt; attr &gt; est une chaîne qui représente un attributeType. La valeur de jeton &lt; &gt; est une chaîne qui représente un AttributeValue dont le format est défini par le service d’annuaire sous-jacent.

Si une &lt; valeur &gt; doit contenir le caractère astérisque ( \* ), de parenthèse ouvrante (() ou de parenthèse fermante ()), le caractère doit être précédé du caractère d’échappement barre oblique inverse ( \\ ).

## <a name="special-characters"></a>Caractères spéciaux

Si l’un des caractères spéciaux suivants doit apparaître dans le filtre de recherche en tant que littéraux, ils doivent être remplacés par la séquence d’échappement indiquée.



| Caractère ASCII | Substitution de séquence d’échappement |
|-----------------|----------------------------|
| \*              | \\2a                       |
| (               | \\28/08/03                       |
| )               | \\28                       |
| \\              | \\5C                       |
| NUL             | \\producteurs                       |
| /               | \\2F                       |



 

> [!Note]  
> Dans les cas où un jeu de caractères multioctets est utilisé, les séquences d’échappement listées ci-dessus doivent être utilisées si la recherche est effectuée par ADO avec le dialecte SQL.

 

En outre, les données binaires arbitraires peuvent être représentées à l’aide de la syntaxe de séquence d’échappement en encodant chaque octet de données binaires avec la barre oblique inverse ( \\ ) suivie de deux chiffres hexadécimaux. Par exemple, la valeur de 4 octets 0x00000004 est encodée sous la forme \\ 00 00 \\ \\ 00 \\ 04 dans une chaîne de filtrage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Dialecte LDAP](ldap-dialect.md)
</dt> <dt>

[Dialecte SQL](sql-dialect.md)
</dt> <dt>

[Recherche avec l’interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Recherche avec OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 
