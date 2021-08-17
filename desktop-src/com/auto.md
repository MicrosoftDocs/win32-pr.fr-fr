---
title: Auto
description: Détermine si le débogueur est automatiquement lancé lors de l’envoi d’une notification RPC COM.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 030cab43fe0ac4a67551920479b9c36f3d1ff33f2ba2854647fcf209cfe694e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737221"
---
# <a name="auto"></a>Auto

Détermine si le débogueur est automatiquement lancé lors de l’envoi d’une notification RPC COM.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **\_ mot reg** .



| Valeur | Description                    |
|-------|--------------------------------|
| 1     | Lancer automatiquement le débogueur. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ dbg \_ tout**](orpc-dbg-all.md)
</dt> </dl>

 

 




