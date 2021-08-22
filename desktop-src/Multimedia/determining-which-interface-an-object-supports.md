---
title: Détermination de l’interface prise en charge par un objet
description: Détermination de l’interface prise en charge par un objet
ms.assetid: cf2aacb7-5315-4907-a49b-3eb3bbfd13d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5afffd2818c7a8f204363180e52fe9f94f16157aacd027582ce377b2f5211c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497255"
---
# <a name="determining-which-interface-an-object-supports"></a>Détermination de l’interface prise en charge par un objet

La méthode **QueryInterface** permet à une application de demander à un objet de déterminer les interfaces qu’il prend en charge. L’exemple d’application définit le pointeur *PPV* sur l’interface actuelle.


```C++
STDMETHODIMP CAVIFileCF::QueryInterface( 
    const IID FAR& iid, 
    void FAR* FAR* ppv) 
{ 
    if (iid == IID_IUnknown) 
        *ppv = this;                     // set the interface pointer 
                                         // to this instance 
    else if (iid == IID_IClassFactory) 
        *ppv = this;                     // second chance to set the 
                                         // interface pointer to this 
                                         // instance 
    else 
        return ResultFromScode(E_NOINTERFACE); 
    AddRef();  //Increment the reference count 
    return NULL; 
} 

```



 

 




