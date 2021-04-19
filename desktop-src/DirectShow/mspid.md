---
description: Notez que cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser. Le type de données MSPID identifie l’objectif d’un flux de média.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537804"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Cette API est déconseillée. Les nouvelles applications ne doivent pas l’utiliser.

 

Le type de données **MSPID** identifie l’objectif d’un flux de média.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Notes

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

 

 




