---
title: Mise en cache des connexions
description: Lorsqu’une connexion à un serveur est établie, le descripteur de connexion est mis en cache sur l’ordinateur client pour ce processus jusqu’à ce que la connexion soit fermée.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- mise en cache des connexions ADSI
- mise en cache des connexions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d102a52be9c7ccf40f9076892a85d5b3b8683
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028565"
---
# <a name="connection-caching"></a>Mise en cache des connexions

Lorsqu’une connexion à un serveur est établie, le descripteur de connexion est mis en cache sur l’ordinateur client pour ce processus jusqu’à ce que la connexion soit fermée. Si le même serveur, le même port et les mêmes informations d’identification sont utilisés dans une connexion suivante et que seuls les indicateurs de liaison **\_ rapide \_ ADS** ou d’authentification de **\_ \_ liaison de serveur ADS** diffèrent, ADSI réutilise la connexion existante. ADSI effectue cette mise en cache des connexions par processus.

Pour améliorer les performances, réutilisez les connexions existantes lorsque cela est possible.

L’exemple de code suivant illustre le fonctionnement de la mise en cache des connexions.


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




