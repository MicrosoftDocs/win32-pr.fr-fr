---
title: Modification d’un objet ADSI à partir d’ADO
description: ADSI pour Windows 2000 et DS client incluent un fournisseur de OLE DB en lecture seule. Cela signifie que vous ne pouvez pas, à l’heure actuelle, émettre l’instruction UPDATE dans le dialecte SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Modification d’un objet ADSI à partir d’ADO ADSI
- ActiveX Data Object ADSI, modification d’un objet ADSI à partir d’ADO
- ADSI ADSI, exemple de code C/C++, modification d’un objet ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671138"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Modification d’un objet ADSI à partir d’ADO

ADSI pour Windows 2000 et DS client incluent un fournisseur de OLE DB en lecture seule. Cela signifie que vous ne pouvez pas, à l’heure actuelle, émettre l’instruction UPDATE dans le dialecte SQL.

**Pour modifier un objet retourné à partir d’une requête ADO**

1.  Demandez le **ADsPath** quand vous spécifiez un nom d’attribut, comme dans « select ADsPath,... »
2.  Exécutez la requête et récupérez l’attribut **ADsPath** .
3.  Établissez une liaison au jeu d’enregistrements à l’aide de **ADsPath** et modifiez les attributs.

L’exemple de code suivant montre comment modifier un objet ADSI après avoir effectué les étapes décrites dans l’exemple précédent.


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




