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
# <a name="modifying-an-adsi-object-from-ado"></a><span data-ttu-id="436fd-107">Modification d’un objet ADSI à partir d’ADO</span><span class="sxs-lookup"><span data-stu-id="436fd-107">Modifying an ADSI Object from ADO</span></span>

<span data-ttu-id="436fd-108">ADSI pour Windows 2000 et DS client incluent un fournisseur de OLE DB en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="436fd-108">ADSI for Windows 2000 and DS Client includes a read-only OLE DB provider.</span></span> <span data-ttu-id="436fd-109">Cela signifie que vous ne pouvez pas, à l’heure actuelle, émettre l’instruction UPDATE dans le dialecte SQL.</span><span class="sxs-lookup"><span data-stu-id="436fd-109">This means that you cannot, at present, issue the UPDATE statement in the SQL dialect.</span></span>

<span data-ttu-id="436fd-110">**Pour modifier un objet retourné à partir d’une requête ADO**</span><span class="sxs-lookup"><span data-stu-id="436fd-110">**To modify an object returned from an ADO query**</span></span>

1.  <span data-ttu-id="436fd-111">Demandez le **ADsPath** quand vous spécifiez un nom d’attribut, comme dans « select ADsPath,... »</span><span class="sxs-lookup"><span data-stu-id="436fd-111">Request the **ADsPath** when specifying an attribute name, as in "SELECT ADsPath, ..."</span></span>
2.  <span data-ttu-id="436fd-112">Exécutez la requête et récupérez l’attribut **ADsPath** .</span><span class="sxs-lookup"><span data-stu-id="436fd-112">Execute the query and get the **ADsPath** attribute.</span></span>
3.  <span data-ttu-id="436fd-113">Établissez une liaison au jeu d’enregistrements à l’aide de **ADsPath** et modifiez les attributs.</span><span class="sxs-lookup"><span data-stu-id="436fd-113">Bind to the record set using **ADsPath**, and modify the attributes.</span></span>

<span data-ttu-id="436fd-114">L’exemple de code suivant montre comment modifier un objet ADSI après avoir effectué les étapes décrites dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="436fd-114">The following code example shows how to modify an ADSI object after performing the steps outlined in the preceding example.</span></span>


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



 

 




