---
title: Création d’une instance de File-Handler dans une DLL
description: Création d’une instance de File-Handler dans une DLL
ms.assetid: 0cf7ef72-c675-4a67-97b3-18cccfb7ddc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0023de28f660473a1747ff05528ec5360674754b5c0bcd34f5ae3a28cc39412f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144752"
---
# <a name="creating-a-file-handler-instance-in-a-dll"></a>Création d’une instance de File-Handler dans une DLL

Lorsqu’une application spécifie la DLL du gestionnaire de fichiers ou le gestionnaire de flux, le système la recherche dans le registre par son identificateur de classe et est chargé. Le système appelle ensuite la fonction [**DllGetClassObject**](/previous-versions//dd797891(v=vs.85)) de la dll pour créer une instance du gestionnaire de fichiers ou de flux. L’exemple suivant (écrit en C++) montre comment un gestionnaire de fichiers crée une instance.


```C++
// Main DLL entry point. 
STDAPI DllGetClassObject(const CLSID FAR& rclsid, 
    const IID FAR& riid, void FAR* FAR* ppv) 
{ 
    HRESULT hresult; 
    hresult = CAVIFileCF::Create(rclsid, riid, ppv); 
    return hresult; 
} 
HRESULT CAVIFileCF::Create(const CLSID FAR&   rclsid, 
    const IID FAR& riid, void FAR* FAR*   ppv) 
{ 
// The following is the class factory creation and not an 
// actual PAVIFile. 
    CAVIFileCF FAR*   pAVIFileCF; 
    IUnknown FAR*   pUnknown; 
    HRESULT hresult; 
 
// Create the instance. 
    pAVIFileCF = new FAR CAVIFileCF(rclsid, &pUnknown); 
    if (pAVIFileCF == NULL) 
        return ResultFromScode(E_OUTOFMEMORY); 
 
// Set the interface pointer. 
    hresult = pUnknown->QueryInterface(riid, ppv); 
    if (FAILED(GetScode(hresult))) 
        delete pAVIFileCF; 
    return hresult; 
} 

```



 

 