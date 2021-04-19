---
title: Méthodes de propriété d’interface
description: De nombreuses interfaces ADSI sont conçues pour prendre en charge l’automatisation et sont donc des interfaces doubles en ce sens qu’elles prennent en charge l’accès client via les interfaces IUnknown et IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété d’interface
- ADSI ADSI, référence, méthodes de propriété expliquées
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510281"
---
# <a name="interface-property-methods"></a>Méthodes de propriété d’interface

De nombreuses interfaces ADSI sont conçues pour prendre en charge l’automatisation et sont donc des interfaces doubles en ce sens qu’elles prennent en charge l’accès client via les interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) et [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Les clients non-Automation, tels que ceux écrits en C/C++, résolvent directement l’appel de méthode, à l’aide de la méthode [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , et appellent la méthode directement. Les clients Automation, également appelés clients liés au nom, tels que ceux écrits en Visual Basic ou Visual Basic Scripting Edition (VBScript), doivent résoudre indirectement l’appel de méthode à l’aide de la méthode [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) .

Une interface ADSI prenant en charge Automation définit des méthodes de propriété pour récupérer et modifier les propriétés d’un objet qui implémente l’interface. Les méthodes de propriété ont des noms qui ont des noms d' **extraction** \_ et de **mise** \_ en avant des noms de propriété appropriés, par exemple, **obtenir un \_ utilisateur** et un **\_ nom de placement**.

Chaque méthode d' **extraction \_** utilise un seul paramètre comme sortie. Ce paramètre est une adresse allouée par méthode d’une variable du type de données de la propriété. Lors du retour, cette variable utilise la valeur actuelle de la propriété demandée. L’appelant doit libérer la mémoire allouée de la variable lorsque la propriété n’est plus nécessaire.

Chaque **méthode \_ put** prend un paramètre unique comme entrée pour le type de données de la propriété correspondante. Le paramètre contient une nouvelle valeur de la propriété.

L’exemple de code suivant montre l’appel des méthodes de propriété qui suivent la procédure habituelle pour appeler la fonction membre d’un objet.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



L’exemple de code suivant montre l’appel des méthodes de propriété dans les clients Automation, qui peuvent être légèrement différents. Par exemple, Visual Basic utilise la notation par points.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Tous les paramètres et types de retour doivent être de ceux définis par le type de données VARIANT. Toutes les méthodes d’une interface double retournent une valeur HRESULT pour indiquer la réussite ou l’échec.

Pour plus d’informations sur l’obtention et la définition des propriétés sur les objets ADSI, consultez [cache des propriétés](property-cache-interfaces.md).

 

 