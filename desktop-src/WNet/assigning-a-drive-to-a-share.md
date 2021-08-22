---
title: Affectation d’un lecteur à un partage
description: L’exemple suivant montre comment connecter une lettre de lecteur à un partage de serveur distant à l’aide d’un appel à la fonction WNetAddConnection2. L’exemple informe l’utilisateur que l’appel a réussi ou non.
ms.assetid: 1533aa5c-c3f3-4bd6-b307-fb4bd4c9aa85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37095f085b3124cfaa049de4bf61ae830c94191c94c5993f7532920b122b63d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053377"
---
# <a name="assigning-a-drive-to-a-share"></a>Affectation d’un lecteur à un partage

L’exemple suivant montre comment connecter une lettre de lecteur à un partage de serveur distant à l’aide d’un appel à la fonction [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) . L’exemple informe l’utilisateur que l’appel a réussi ou non.

Pour tester l’exemple de code suivant, procédez comme suit :

1.  Remplacez les lignes suivantes par des chaînes valides :

    ``` syntax
    szUserName[32] = "myUserName",
    szPassword[32] = "myPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
    ```

2.  Ajoutez le fichier à une application console appelée AddConn2.
3.  Liez la bibliothèque MPR. LIB vers la liste de bibliothèques du compilateur.
4.  Compilez et exécutez le programme AddConn2.EXE.


```C++
#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>
#pragma comment(lib, "mpr.lib")

void main()
{
NETRESOURCE nr;
DWORD res;
TCHAR szUserName[32] = "MyUserName",
    szPassword[32] = "MyPassword",
    szLocalName[32] = "Q:",
    szRemoteName[MAX_PATH] = "\\\\products2\\relsys";
//
// Assign values to the NETRESOURCE structure.
//
nr.dwType = RESOURCETYPE_ANY;
nr.lpLocalName = szLocalName;
nr.lpRemoteName = szRemoteName;
nr.lpProvider = NULL;
//
// Call the WNetAddConnection2 function to assign
//   a drive letter to the share.
//
res = WNetAddConnection2(&nr, szPassword, szUserName, FALSE);
//
// If the call succeeds, inform the user; otherwise,
//  print the error.
//
if(res == NO_ERROR)
  printf("Connection added \n", szRemoteName);
else
  printf("Error: %ld\n", res);
  return;
}
```



 

 