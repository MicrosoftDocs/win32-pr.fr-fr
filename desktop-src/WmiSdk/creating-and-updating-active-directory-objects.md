---
description: Les objets Active Directory peuvent être utilisés pour localiser des ressources dans un domaine de réseau d’ordinateurs, telles que des utilisateurs, des stratégies de sécurité, des imprimantes, des composants distribués et d’autres ressources.
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: Création et mise à jour d’objets Active Directory
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0b36a12860ea2c2dc9085b784fdaf85cd95ab87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521509"
---
# <a name="creating-and-updating-active-directory-objects"></a>Création et mise à jour d’objets Active Directory

Les objets Active Directory peuvent être utilisés pour localiser des ressources dans un domaine de réseau d’ordinateurs, telles que des utilisateurs, des stratégies de sécurité, des imprimantes, des composants distribués et d’autres ressources. Les objets Active Directory peuvent être créés et mis à jour à l’aide de WMI. Vous pouvez mettre à jour un objet Active Directory lorsque de nouvelles informations sur l’objet deviennent disponibles à l’aide de la notification d’événement WMI. Par exemple, une fois qu’un objet utilisateur Active Directory est créé, vous pouvez détecter sa création à l’aide d’une requête d’événement dans WMI et, lorsque l’événement est reçu, vous pouvez mettre à jour l’objet avec de nouvelles informations.

L’exemple de code suivant crée une nouvelle instance WMI de la classe qui représente l’objet utilisateur Active Directory. L’exemple montre comment assigner des valeurs à différentes propriétés requises pour créer la nouvelle instance de Active Directory utilisateur.


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



L’exemple de code suivant met à jour une instance WMI d’un objet Active Directory. Dans cet exemple, l’attribut DisplayName est mis à jour.


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



