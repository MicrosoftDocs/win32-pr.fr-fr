---
title: Interface (COM)
description: Entrée facultative qui spécifie tous les ID d’interface (IID) pris en charge par la classe associée.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Clé de registre de l’interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048117"
---
# <a name="interface-com"></a>Interface (COM)

Entrée facultative qui spécifie tous les ID d’interface (IID) pris en charge par la classe associée.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Remarques

Si un nom d’interface n’est pas présent dans cette liste, l’interface ne peut jamais être prise en charge par une instance de cette classe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clé d'interface](interface-key.md)
</dt> </dl>

 

 




