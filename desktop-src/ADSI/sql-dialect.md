---
title: Dialecte SQL
description: Le dialecte SQL, dérivé de l’langage SQL, utilise des expressions explicites pour définir des instructions de requête.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- Langage SQL (ADSI)
- dialecte ADSI, dialecte SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508956"
---
# <a name="sql-dialect"></a>Dialecte SQL

Le dialecte SQL, dérivé de l’langage SQL, utilise des expressions explicites pour définir des instructions de requête. Utilisez une instruction de requête SQL avec les interfaces de recherche ADSI suivantes :

-   Interfaces [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , qui sont des interfaces Automation qui utilisent OLE DB.
-   [OLE DB](searching-with-ole-db.md), qui est un ensemble d’interfaces C/C++ pour interroger des bases de données.

Les instructions SQL requièrent la syntaxe suivante.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



Le tableau suivant répertorie les mots clés des instructions de requête SQL.



| Mot clé  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Spécifie une liste d’attributs séparés par des virgules à récupérer pour chaque objet. Si vous spécifiez \* , la requête récupère uniquement l’ADsPath de chaque objet.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Spécifie l’ADsPath de la base de la recherche. Par exemple, l’ADsPath du conteneur Users dans un domaine Active Directory peut être’LDAP :As = Users, DC = fabrikam, DC = COM'. Notez que le chemin d’accès est placé entre deux guillemets simples (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Mot clé facultatif qui spécifie le filtre de requête.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Mot clé facultatif qui génère un tri côté serveur si le serveur prend en charge le contrôle de tri LDAP. Active Directory prend en charge le contrôle de tri, mais il peut avoir un impact sur les performances du serveur, en particulier si le jeu de résultats est volumineux. La liste de tri est une liste séparée par des virgules d’attributs sur lesquels effectuer le tri. N’oubliez pas que Active Directory ne prend en charge qu’une seule clé de tri. Vous pouvez utiliser les mots clés facultatifs ASC et DESC pour spécifier l’ordre de tri croissant ou décroissant ; la valeur par défaut est l’ordre croissant. Le mot clé ORDER BY remplace toute clé de tri spécifiée par la propriété « sort on » de l’objet Command ADO. |



 

> [!Note]  
> Dans les cas où un jeu de caractères multioctets est utilisé, si la recherche est effectuée par ADO avec le dialecte SQL, une barre oblique inverse ne peut pas être utilisée pour échapper des caractères. Au lieu de cela, les séquences d’échappement listées dans les [caractères spéciaux](search-filter-syntax.md) doivent être utilisées. Par exemple, pour une instruction qui a utilisé la syntaxe « samAccountName = \( test », qui utilise la barre oblique inverse « \\ », pour échapper la parenthèse ouvrante « ( », à la place, vous devez remplacer la barre oblique inverse par le caractère spécial « \\ 28 », comme suit : « sAMAccountName = \\ 28Test ».

 

Les instructions de requête suivantes sont des exemples de dialecte SQL dans ADSI.

Pour rechercher tous les objets de groupe.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Pour rechercher tous les utilisateurs dont le nom commence par la lettre H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



La grammaire formelle pour les requêtes SQL est définie dans l’exemple de code suivant. Tous les mots clés ne respectent pas la casse.


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



Les jointures internes SQL ne sont pas prises en charge par le fournisseur de OLE DB Active Directory, mais vous pouvez utiliser SQL pour joindre des données SQL et Active Directory. Pour plus d’informations, consultez [création d’une jointure hétérogène entre SQL Server et Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe de filtre de recherche](search-filter-syntax.md)
</dt> <dt>

[Dialecte LDAP](ldap-dialect.md)
</dt> <dt>

[Recherche avec l’interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Recherche avec OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




