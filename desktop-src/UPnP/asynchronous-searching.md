---
title: Recherche asynchrone
description: L’objet de recherche d’appareils active les recherches synchrones et asynchrones. Les recherches asynchrones retournent immédiatement le contrôle à l’application appelante.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940241"
---
# <a name="asynchronous-searching"></a><span data-ttu-id="cf734-104">Recherche asynchrone</span><span class="sxs-lookup"><span data-stu-id="cf734-104">Asynchronous Searching</span></span>

<span data-ttu-id="cf734-105">L’objet de recherche d’appareils active les recherches synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="cf734-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="cf734-106">Les recherches asynchrones retournent immédiatement le contrôle à l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="cf734-106">Asynchronous searches return control to the calling application immediately.</span></span> <span data-ttu-id="cf734-107">Ensuite, l’application est notifiée de chaque appareil individuel à mesure qu’elle est trouvée, à l’aide d’une interface de rappel enregistrée par l’application.</span><span class="sxs-lookup"><span data-stu-id="cf734-107">Then, the application is notified about each individual device as it is found, using a callback interface that the application has registered.</span></span>

<span data-ttu-id="cf734-108">La recherche asynchrone est idéale pour les interfaces utilisateur graphiques, et pour les applications qui effectuent une surveillance continue.</span><span class="sxs-lookup"><span data-stu-id="cf734-108">Asynchronous searching is best for graphical user interfaces, and applications that perform continuous monitoring.</span></span>

<span data-ttu-id="cf734-109">La structure générale d’une recherche asynchrone est la suivante :</span><span class="sxs-lookup"><span data-stu-id="cf734-109">The general structure of an asynchronous search is:</span></span>

1.  <span data-ttu-id="cf734-110">Créer un objet de recherche</span><span class="sxs-lookup"><span data-stu-id="cf734-110">Create a search object</span></span>
2.  <span data-ttu-id="cf734-111">Démarrer la recherche</span><span class="sxs-lookup"><span data-stu-id="cf734-111">Start the search</span></span>
3.  <span data-ttu-id="cf734-112">Recevez des notifications de rappel et suivez les étapes de traitement appropriées.</span><span class="sxs-lookup"><span data-stu-id="cf734-112">Receive callback notifications and take the appropriate processing steps.</span></span>
4.  <span data-ttu-id="cf734-113">Lorsque la recherche n’est plus nécessaire, annulez la recherche et relâchez les objets associés.</span><span class="sxs-lookup"><span data-stu-id="cf734-113">When the search is no longer needed, cancel the search and release the associated objects.</span></span>

> [!Note]  
> <span data-ttu-id="cf734-114">Dans le code de rappel, une application ne peut pas libérer l’objet sur lequel elle reçoit une notification, tel qu’un nouvel appareil, et l’application ne peut pas annuler la recherche.</span><span class="sxs-lookup"><span data-stu-id="cf734-114">In the callback code, an application cannot release the object it is receiving notification about, such as a new device, nor can the application cancel the search.</span></span>

 

## <a name="c-example"></a><span data-ttu-id="cf734-115">Exemple C++</span><span class="sxs-lookup"><span data-stu-id="cf734-115">C++ Example</span></span>

<span data-ttu-id="cf734-116">Les applications C++ doivent implémenter un objet de rappel à passer à la recherche.</span><span class="sxs-lookup"><span data-stu-id="cf734-116">C++ applications must implement a callback object to pass to the search.</span></span> <span data-ttu-id="cf734-117">Pour obtenir un exemple de code illustrant cette action, consultez [recherche asynchrone en C++](searching-asynchronously-in-c-.md) .</span><span class="sxs-lookup"><span data-stu-id="cf734-117">See [Searching Asynchronously in C++](searching-asynchronously-in-c-.md) for sample code that illustrates this action.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="cf734-118">Exemple VBScript</span><span class="sxs-lookup"><span data-stu-id="cf734-118">VBScript Example</span></span>

<span data-ttu-id="cf734-119">Le code VBScript doit passer l’adresse de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="cf734-119">VBScript code must pass the address of the callback function.</span></span>


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



 

 




