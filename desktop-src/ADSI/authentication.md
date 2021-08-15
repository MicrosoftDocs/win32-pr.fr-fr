---
title: Authentification (ADSI)
description: Dans ADSI, les informations d’identification qui se composent d’un nom d’utilisateur et d’un mot de passe sont utilisées pour fournir ou restreindre l’accès aux objets dans le service d’annuaire.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- Authentification ADSI
- ADSI, utilisation, authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840556"
---
# <a name="authentication-adsi"></a>Authentification (ADSI)

Dans ADSI, les informations d’identification qui se composent d’un nom d’utilisateur et d’un mot de passe sont utilisées pour fournir ou restreindre l’accès aux objets dans le service d’annuaire. La fonction [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) utilise les informations d’identification du thread appelant pour l’authentification. La fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) peuvent être utilisées pour spécifier des informations d’identification autres que celles du thread appelant. Lorsqu’un objet est lié à avec un utilisateur authentifié, l’utilisateur est autorisé à accéder à l’objet tel qu’il est pris en charge par les exigences de sécurité du service d’annuaire sous-jacent.

> [!Note]  
> La fonction [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) et la méthode [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ne doivent pas être utilisées pour valider les informations d’identification de l’utilisateur. Pour plus d’informations sur la validation des informations d’identification de l’utilisateur, consultez l’article 180548 de la base de connaissances Microsoft [Comment : valider les informations d’identification de l’utilisateur sur les systèmes d’exploitation Microsoft](https://support.microsoft.com/kb/180548).

 

L’exemple de code suivant montre comment utiliser la méthode [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) pour authentifier un utilisateur.


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




