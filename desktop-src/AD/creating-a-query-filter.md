---
title: Création d’un filtre de requête
description: Un filtre de requête demande à Active Directory Domain Services de rechercher des données dans une syntaxe de requête LDAP. Toutes les technologies d’accès aux données indiquées dans la rubrique choix de la technologie de recherche prennent en charge la syntaxe de requête LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Active Directory des exemples Active Directory, création d’un filtre de requête
- filtres de requête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839086"
---
# <a name="creating-a-query-filter"></a>Création d’un filtre de requête

Un filtre de requête demande à Active Directory Domain Services de rechercher des données dans une syntaxe de requête LDAP. Toutes les technologies d’accès aux données indiquées dans la rubrique [choix de la technologie de recherche](choosing-the-search-technology.md) prennent en charge la syntaxe de requête LDAP.

La syntaxe de la requête LDAP est la suivante :


```C++
<expression><expression>...
```



Un filtre peut contenir une ou plusieurs expressions. Une expression se présente sous la forme suivante :


```C++
(<logicaloperator><comparison><comparison...>)
```



où « &lt; LogicalOperator &gt; » est l’un des éléments suivants.



| Opérateur        | Description                |
|-----------------|----------------------------|
| "\|"<br/> | **Ou** logique<br/>  |
| "&"<br/>  | **And** logique<br/> |
| "!"<br/>  | **Not** logique<br/> |



 

et « &lt; comparaison &gt; » est le suivant :


```C++
(<attribute><operator><value>)
```



où « &lt; attribute &gt; » est le **lDAPDisplayName** de l’attribut à évaluer, « &lt; value &gt; » est la valeur à comparer et « &lt; Operator &gt; » est l’un des opérateurs de comparaison suivants.



| Opérateur           | Description                         |
|--------------------|-------------------------------------|
| "="<br/>     | Égal à<br/>                   |
| "~="<br/>    | Approximativement égal à<br/>     |
| "<="<br/> | Inférieur ou égal à<br/>    |
| ">="<br/> | Supérieur ou égal à<br/> |



 

En outre, selon la syntaxe d’attribut, la « &lt; valeur &gt; » peut contenir le caractère générique (« \* »). Une « &lt; valeur &gt; » qui contient uniquement un caractère générique vérifie l’existence d’une valeur dans « &lt; attribut &gt; ». Si aucune valeur n’est définie pour « &lt; attribute &gt; », le test échoue.

Si l’un des caractères spéciaux suivants doit apparaître dans le filtre de requête comme littéraux, ils doivent être remplacés par la séquence d’échappement répertoriée.



| Caractère ASCII    | Substitution de séquence d’échappement |
|--------------------|----------------------------|
| \*<br/>      | « \\ 2A »<br/>          |
| (<br/>       | " \\ 28"<br/>          |
| )<br/>       | « \\ 29 »<br/>          |
| \\<br/>      | « \\ 5C »<br/>          |
| **NUL**<br/> | « \\ 00 »<br/>          |



 

En outre, les données binaires arbitraires peuvent être représentées à l’aide de la syntaxe de séquence d’échappement en encodant chaque octet de données binaires avec la barre oblique inverse suivie de deux chiffres hexadécimaux. Par exemple, la valeur de 4 octets 0x00000004 est encodée sous la forme « \\ 00 \\ 00 \\ 00 \\ 04 » dans une chaîne de filtrage.

## <a name="examples"></a>Exemples

La chaîne de requête suivante recherche tous les objets de type « Computer ».


```C++
(objectCategory=computer)
```



La chaîne de requête suivante recherche tous les objets de type « Computer » dont le nom commence par « Desktop ».


```C++
(&(objectCategory=computer)(name=desktop*))
```



La chaîne de requête suivante recherche tous les objets de type « Computer » dont le nom commence par « Desktop » ou un nom commençant par « Notebook ».


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



La chaîne de requête suivante recherche tous les objets de type « utilisateur » qui ont un numéro de téléphone privé.


```C++
(&(objectCategory=user)(homePhone=*))
```



Pour plus d’informations sur les chaînes de filtre de requête et des exemples d’utilisation, consultez :

-   [Rechercher des objets par classe](finding-objects-by-class.md)
-   [Recherche d’objets par nom](finding-objects-by-name.md)
-   [Recherche d’une liste d’attributs à interroger](finding-a-list-of-attributes-to-query.md)
-   [Vérification de la syntaxe du filtre de requête](checking-the-query-filter-syntax.md)
-   [Comment spécifier des valeurs de comparaison](how-to-specify-comparison-values.md)

 

 





