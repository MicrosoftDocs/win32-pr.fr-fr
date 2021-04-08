---
title: Recherche d’objets
description: Julie Bankert doit trouver les numéros de téléphone de tous les chefs de programme qui travaillent dans le service 101. Elle peut créer un script qui utilise ADO et ADSI pour y parvenir.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- recherche d’objets ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103841926"
---
# <a name="searching-for-objects"></a>Recherche d’objets

Julie Bankert doit trouver les numéros de téléphone de tous les chefs de programme qui travaillent dans le service 101. Elle peut créer un script qui utilise ADO et ADSI pour y parvenir.

Lorsque vous utilisez le fournisseur ADO pour exécuter une requête, le jeu de résultats retourne uniquement les premiers 1000 objets. Pour cette raison, il est important d’utiliser une requête paginée afin de pouvoir récupérer tous les objets du jeu de résultats, tant que le service d’annuaire n’a pas été défini pour limiter le nombre d’éléments dans un jeu de résultats. Les jeux de retours contiendront le nombre d’éléments que vous spécifiez dans la taille de la page, et les jeux paginés continueront à être retournés jusqu’à ce que tous les éléments du jeu de résultats aient été retournés.


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



Pour effectuer une recherche ADSI dans Visual Basic ou dans un environnement de script, trois composants ADO sont requis : **connexion**, **commande** et **Recordset**. L’objet de **connexion** vous permet de spécifier le nom du fournisseur, les autres informations d’identification, le cas échéant, ainsi que d’autres indicateurs. L’objet **Command** vous permet de spécifier des préférences de recherche et la chaîne de requête. Vous devez associer l’objet de **connexion** à un objet de **commande** avant l’exécution de la requête. Enfin, l’objet **Recordset** est utilisé pour itérer le jeu de résultats.

ADSI prend en charge deux types de chaînes de requête ou de dialectes. L’exemple de code précédent utilise le dialecte SQL. Vous pouvez également utiliser le dialecte LDAP. La chaîne de requête de dialecte LDAP est basée sur la [norme rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (une RFC est un document de demande de commentaires, qui est la base du développement de normes LDAP). L’exemple précédent peut être traduit dans l’exemple de code suivant.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Pourquoi le mot « sous-arbre » se trouve-t-il à la fin de la chaîne ? Dans le monde de l’annuaire, vous pouvez spécifier l’étendue de la recherche. Les choix sont les suivants : « base », « onelevel » et « sous-arborescence ». « base » est utilisé pour lire l’objet lui-même ; « onelevel » fait référence aux enfants immédiats, similaires à la commande **dir** . « sous-arborescence » permet d’effectuer des recherches sur plusieurs niveaux (comme **dir/s**).

Avec le dialecte SQL, vous pouvez spécifier la portée dans la propriété Command, comme dans l’exemple de code suivant.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Si l’étendue n’est pas spécifiée, par défaut, elle utilise une recherche de sous-arborescence.

> [!Note]  
> Si vous utilisez C++, vous pouvez utiliser l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) à partir d’ADSI.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réorganisation](reorganization.md)
</dt> </dl>

 

 




