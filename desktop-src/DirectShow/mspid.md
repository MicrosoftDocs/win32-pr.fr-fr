---
description: Notez que cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser. Le type de données MSPID identifie l’objectif d’un flux de média.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d274fc4131c0aa4494d610cbe1145ad79b848b5f6280d4ad6a10b298a8b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075749"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser.

 

Le type de données **MSPID** identifie l’objectif d’un flux de média.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Remarques

**MSPID** est simplement un typedef pour GUID. Les MSPIDs suivants sont définis.



| Valeur               | Description           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | Flux vidéo principal. |
| MSPID \_ PrimaryAudio | Flux audio principal. |



 

Le type **REFMSPID** définit une référence à un **MSPID**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Mmstream. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données de diffusion multimédia](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




