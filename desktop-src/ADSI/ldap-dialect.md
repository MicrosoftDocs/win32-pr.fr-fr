---
title: Dialecte LDAP
description: Le dialecte LDAP est un format pour les instructions de requête qui utilisent la syntaxe de filtre de recherche LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- Interface ADSI de dialecte LDAP
- dialectes ADSI, dialecte LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122141"
---
# <a name="ldap-dialect"></a>Dialecte LDAP

Le dialecte LDAP est un format pour les instructions de requête qui utilisent la [syntaxe de filtre de recherche LDAP](search-filter-syntax.md). Utilisez une instruction de requête LDAP avec les interfaces de recherche ADSI suivantes :

-   interfaces d' [objets de données ActiveX (ADO)](searching-with-activex-data-objects-ado.md) , qui sont des interfaces Automation qui utilisent des OLE DB.
-   [OLE DB](searching-with-ole-db.md), qui est un ensemble d’interfaces C/C++ pour interroger des bases de données.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), qui est l’interface C/C++ pour Active Directory.

Une chaîne de dialecte LDAP se compose de quatre parties séparées par des points-virgules (;).

-   Nom unique de base. Par exemple :

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Filtres de recherche LDAP. Pour plus d’informations sur les filtres de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).
-   Nom complet LDAP des attributs à récupérer. Plusieurs attributs sont séparés par une virgule.
-   Spécifie l’étendue de la recherche. Les valeurs valides sont « base », « onelevel » et « sous-arborescence ». L’étendue spécifiée dans une chaîne de requête LDAP remplace toute étendue de recherche spécifiée par la propriété « SearchScope » de l’objet de commande ADO.

Voici un exemple de code du dialecte LDAP dans ADSI qui effectue une recherche dans tous les objets de la sous-arborescence.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Toutes les options de recherche (taille de page de recherche, par exemple) ne peuvent pas être exprimées dans le dialecte LDAP. vous devez donc définir les options avant le démarrage de l’exécution de la requête réelle.

## <a name="example-code-for-performing-an-ldap-query"></a>Exemple de code pour exécuter une requête LDAP

L’exemple de code suivant montre comment utiliser une requête LDAP.


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



Pour plus d’informations sur la syntaxe de requête, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe de filtre de recherche](search-filter-syntax.md)
</dt> <dt>

[dialecte SQL](sql-dialect.md)
</dt> <dt>

[Recherche avec l’interface IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Recherche avec OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




