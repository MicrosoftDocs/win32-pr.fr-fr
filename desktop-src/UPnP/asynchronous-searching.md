---
title: Recherche asynchrone
description: L’objet de recherche d’appareils active les recherches synchrones et asynchrones. Les recherches asynchrones retournent immédiatement le contrôle à l’application appelante.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3482e041798db929d1719e1a404823f161f9bf5b0e499f4eca1694df24b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058137"
---
# <a name="asynchronous-searching"></a>Recherche asynchrone

L’objet de recherche d’appareils active les recherches synchrones et asynchrones. Les recherches asynchrones retournent immédiatement le contrôle à l’application appelante. Ensuite, l’application est notifiée de chaque appareil individuel à mesure qu’elle est trouvée, à l’aide d’une interface de rappel enregistrée par l’application.

La recherche asynchrone est idéale pour les interfaces utilisateur graphiques, et pour les applications qui effectuent une surveillance continue.

La structure générale d’une recherche asynchrone est la suivante :

1.  Créer un objet de recherche
2.  Démarrer la recherche
3.  Recevez des notifications de rappel et suivez les étapes de traitement appropriées.
4.  Lorsque la recherche n’est plus nécessaire, annulez la recherche et relâchez les objets associés.

> [!Note]  
> Dans le code de rappel, une application ne peut pas libérer l’objet sur lequel elle reçoit une notification, tel qu’un nouvel appareil, et l’application ne peut pas annuler la recherche.

 

## <a name="c-example"></a>Exemple C++

Les applications C++ doivent implémenter un objet de rappel à passer à la recherche. Pour obtenir un exemple de code illustrant cette action, consultez [recherche asynchrone en C++](searching-asynchronously-in-c-.md) .

## <a name="vbscript-example"></a>Exemple VBScript

Le code VBScript doit passer l’adresse de la fonction de rappel.


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




