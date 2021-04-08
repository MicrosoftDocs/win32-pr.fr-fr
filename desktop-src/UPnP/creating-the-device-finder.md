---
title: Création du Finder d’appareils
description: Les exemples suivants montrent comment créer une instance de l’objet Device Finder en C++, Visual Basic et VBScript.
ms.assetid: 0084a64d-458e-471c-a6be-aeb6ed0962d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a12fc7e269f2c0ce5b577fe2f49b6d13fe3b5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840530"
---
# <a name="creating-the-device-finder"></a>Création du Finder d’appareils

Les exemples suivants montrent comment créer une instance de l’objet Device Finder en C++, Visual Basic et VBScript. Les langages de script utilisent l’ID programmatique (ProgID) [**UPnP. UPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) pour identifier la classe Device Finder. Le code C++ utilise l’identificateur de classe.

## <a name="c-example"></a>Exemple C++


```C++
HRESULT hr = S_OK;
IUPnPDeviceFinder *pDeviceFinder = NULL;

hr = CoCreateInstance(CLSID_UPnPDeviceFinder, 
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IUPnPDeviceFinder,
                      (void **) &pDeviceFinder);
```



Comme l’indique cet exemple C++, l’objet de recherche d’appareil expose une interface par défaut, [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder). Les méthodes de cette interface effectuent des recherches en fonction des critères de recherche valides pour un périphérique UPnP. Cette interface étant capable d’automatiser, ses méthodes peuvent être appelées par du code de script.

## <a name="vbscript-example"></a>Exemple VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )
```



 

 




