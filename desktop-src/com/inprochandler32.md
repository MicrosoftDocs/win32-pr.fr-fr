---
title: InprocHandler32
description: Spécifie si une application utilise un gestionnaire personnalisé.
ms.assetid: da611bb6-1f69-449a-9821-e2fbbe413a97
keywords:
- Clé de Registre InprocHandler32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c918669aa3de1c8cf2622e3caf4acc9ae18f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379716"
---
# <a name="inprochandler32"></a>InprocHandler32

Spécifie si une application utilise un gestionnaire personnalisé.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler32 = handler.dll
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le gestionnaire personnalisé utilisé par l’application. Si un gestionnaire personnalisé n’est pas utilisé, l’entrée doit être définie sur Ole32.dll.

Si un conteneur recherche un gestionnaire personnalisé dans le registre, la version 16 bits a la priorité sur un conteneur de 16 bits et la version 32 bits a la priorité sur un conteneur de 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InprocHandler**](inprochandler.md)
</dt> </dl>

 

 




