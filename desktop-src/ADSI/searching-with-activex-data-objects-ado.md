---
title: Rechercher à l’aide d’ActiveX Data Objects (ADO)
description: Le modèle ADO (ActiveX Data Object) se compose d’objets listés dans le tableau suivant.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, recherche avec ADO
- Recherche avec ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106513556"
---
# <a name="searching-with-activex-data-objects-ado"></a>Rechercher à l’aide d’ActiveX Data Objects (ADO)

Le modèle ADO (ActiveX Data Object) se compose d’objets listés dans le tableau suivant.



| Object         | Description                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Connection** | Connexion ouverte à une source de données OLE DB telle que ADSI.                                                                          |
| **Commande**    | Définit une commande spécifique à exécuter sur la source de données.                                                                         |
| **Paramètre**  | Collection facultative pour tous les paramètres à fournir à l’objet de commande.                                                        |
| **RecordSet**  | Ensemble d’enregistrements d’une table, d’un objet de commande ou d’une syntaxe SQL. Un jeu d’enregistrements peut être créé sans objet de connexion sous-jacent. |
| **Champ**      | Une seule colonne de données dans un jeu d’enregistrements.                                                                                            |
| **Propriété**   | Collection de valeurs fournies par le fournisseur pour ADO.                                                                           |
| **Error**      | Contient des données sur les erreurs d’accès aux données. Actualisation lorsqu’une erreur se produit en une seule opération.                                      |



 

Pour qu’ADO communique avec ADSI, il doit y avoir au moins deux objets ADO : **Connection** et **Recordset**. Ces objets ADO servent à authentifier les utilisateurs et à énumérer les résultats, respectivement. En règle générale, vous allez également utiliser un objet de **commande** pour maintenir une connexion active, spécifier des paramètres de requête, tels que la taille de page et l’étendue de recherche, et exécuter une requête. Pour plus d’informations sur la syntaxe de filtre de recherche, consultez [syntaxe de filtre de recherche](search-filter-syntax.md).

L’objet de **connexion** charge le fournisseur OLE DB et valide les informations d’identification de l’utilisateur. Dans Visual Basic, appelez la fonction **CreateObject** avec «ADODB. Connexion» pour créer une instance d’un objet de **connexion** , puis définissez la propriété **Provider** de l’objet de **connexion** sur « ADSDSOObject ». ADODB. Connection» est le ProgID de l’objet **Connection** et « ADSDSOObject » est le nom du fournisseur OLE DB dans ADSI. Si aucune information d’identification n’est spécifiée, les informations d’identification de l’utilisateur actuellement connecté sont utilisées.

L’exemple de code suivant montre comment créer une instance d’un objet de **connexion** .


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



L’exemple de code suivant montre comment créer une instance d’un objet de **connexion** .


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



L’exemple de code suivant montre comment créer une instance d’un objet de **connexion** . N’oubliez pas que vous devez inclure la bibliothèque de types ADO (msadoXX.dll) comme l’une des références dans le projet Visual Basic.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Spécifiez les données d’authentification de l’utilisateur en définissant les propriétés de l’objet de **connexion** . Le tableau suivant répertorie les propriétés d’authentification utilisateur prises en charge par ADSI.



| Propriété           | Description                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| « ID utilisateur »          | Chaîne qui identifie l’utilisateur dont le contexte de sécurité est utilisé lors de l’exécution de la recherche. Pour plus d’informations sur le format de la chaîne de nom d’utilisateur, consultez [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). S’il n’est pas spécifié, la valeur par défaut est l’utilisateur connecté, ou l’utilisateur représenté par le processus appelant. |
| « Mot de passe »         | Chaîne qui spécifie le mot de passe de l’utilisateur identifié par « ID d’utilisateur ».                                                                                                                                                                                                                                                                      |
| « Chiffrer le mot de passe » | Valeur booléenne qui spécifie si le mot de passe est chiffré. La valeur par défaut est **false**.                                                                                                                                                                                                                                                    |
| « Indicateur ADSI »        | Ensemble d’indicateurs de l’énumération [**\_ d' \_ énumération d’authentification ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) qui spécifient les options d’authentification de liaison. La valeur par défaut est zéro.                                                                                                                                                                         |



 

L’exemple de code suivant montre comment les propriétés sont définies avant la création de l’objet de **commande** .


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



Le deuxième objet ADO est l’objet **Command** . L’identificateur de programme (ProgID) de l’objet **Command** est « ADODB. Command ». Cet objet vous permet d’émettre des instructions de requête et d’autres commandes à ADSI à l’aide de la connexion active. L’objet **Command** utilise sa propriété **ActiveConnection** pour maintenir une connexion active. Elle gère également la propriété **CommandText** pour contenir des instructions de requête émises par un utilisateur. Les instructions de requête sont exprimées dans le dialecte [SQL](sql-dialect.md) ou le [dialecte LDAP](ldap-dialect.md).

Les exemples de code suivants montrent comment créer un objet de **commande** .


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



Dans l’exemple de code suivant, incluez la bibliothèque de types ADO (msadoXX.dll) comme l’une des références.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



Les options de recherche pour l’objet de **commande** sont spécifiées en définissant la propriété **Properties** . Le tableau suivant répertorie les propriétés nommées acceptables pour les **Propriétés**.



| Propriété nommée      | Description                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Synchrone      | Valeur booléenne qui spécifie si la recherche est synchrone ou asynchrone. La valeur par défaut est false (synchrone). Une recherche synchrone bloque jusqu’à ce que le serveur retourne l’intégralité du résultat, ou pour une recherche paginée, la page entière. Une recherche asynchrone se bloque jusqu’à ce qu’une ligne des résultats de la recherche soit disponible ou jusqu’à ce que l’heure spécifiée par la propriété « Timeout » soit écoulée.                           |
| « Résultats du cache »     | Valeur booléenne qui spécifie si le résultat doit être mis en cache côté client. La valeur par défaut est **true**. L’interface ADSI met en cache le jeu de résultats. La désactivation de cette option peut être souhaitable pour les jeux de résultats volumineux.                                                                                                                                                                                                    |
| « Débusquer les références »   | Valeur de l' [**\_ \_ \_ énumération de références Chase ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) qui spécifie la manière dont la recherche repère les références. La valeur par défaut est les références de la **\_ Chase ADS \_ \_ jamais**. Pour plus d’informations sur cette propriété, consultez [références](/windows/desktop/AD/referrals).<br/>                                                                                                                                           |
| « Noms de colonnes uniquement » | Valeur booléenne qui indique que la recherche doit récupérer uniquement le nom des attributs auxquels des valeurs ont été assignées. La valeur par défaut est **false**.                                                                                                                                                                                                                                                       |
| « Alias de Deref »     | Valeur booléenne qui spécifie si les alias des objets trouvés sont résolus. La valeur par défaut est **false**.                                                                                                                                                                                                                                                                                                        |
| « Taille de la page »         | Valeur entière qui active la pagination et spécifie le nombre maximal d’objets à retourner dans un jeu de résultats. La valeur par défaut est aucune taille de page. Pour plus d’informations, consultez [récupération de jeux de résultats volumineux](retrieving-large-results-sets.md).                                                                                                                                                                       |
| SearchScope       | Valeur de l’énumération [**\_ SCOPEENUM ADS**](/windows/win32/api/iads/ne-iads-ads_scopeenum) qui spécifie la zone de recherche. La valeur par défaut est la **\_ sous- \_ arborescence étendue ADS**.                                                                                                                                                                                                                                                                  |
| « Limite de taille »        | Valeur entière qui spécifie la limite de taille pour la recherche. Par Active Directory, la limite de taille spécifie le nombre maximal d’objets retournés. Le serveur arrête la recherche lorsque la limite de taille est atteinte et retourne les résultats accumulés. La valeur par défaut est aucune limite.                                                                                                                                  |
| « Trier sur »           | Chaîne qui spécifie une liste d’attributs séparés par des virgules à utiliser comme clés de tri. Cette propriété fonctionne uniquement pour les serveurs d’annuaire qui prennent en charge le contrôle LDAP pour le tri côté serveur. Active Directory prend en charge le contrôle de tri, mais il peut avoir un impact sur les performances du serveur, en particulier si le jeu de résultats est volumineux. N’oubliez pas que Active Directory ne prend en charge qu’une seule clé de tri. La valeur par défaut est aucun tri. |
| « Limite de temps »        | Valeur entière qui spécifie la limite de temps, en secondes, pour la recherche. Lorsque la limite de temps est atteinte, le serveur arrête la recherche et retourne les résultats accumulés. La valeur par défaut est aucune limite de durée.                                                                                                                                                                                                      |
| Expiré           | Valeur entière qui spécifie la valeur du délai d’attente côté client, en secondes. Cette valeur indique l’heure à laquelle le client attend les résultats du serveur avant d’arrêter la recherche. La valeur par défaut est aucun délai d’attente.                                                                                                                                                                                                  |



 

L’exemple de code suivant montre comment définir des options de recherche.


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



Le troisième objet ADO est **Recordset**. Vous obtenez cet objet lorsque vous appelez la méthode **Execute** sur un objet **Command** . La fonction principale de l’objet **Recordset** consiste à énumérer le jeu de résultats et à obtenir les données. Le jeu de résultats peut contenir des valeurs pour les attributs qui ont une ou plusieurs valeurs. L’obtention d’un attribut à valeur unique est simple, similaire à l’obtention de la valeur de colonne dans la base de données relationnelle, par exemple :


```VB
Fields('name').Value
```



Toutefois, l’obtention d’un attribut avec plusieurs valeurs est plus complexe. Dans ce cas, le **champ. Value** est un tableau et vous devez vérifier les limites inférieure et supérieure du tableau, comme indiqué dans l’exemple de code suivant.


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



L’exemple de code suivant désactive les comptes d’utilisateur sur un serveur LDAP.


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



Pour plus d’informations sur le modèle objet ADO, consultez [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).

 

