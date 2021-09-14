---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY est un type utilisé pour définir un tableau de correctifs MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110866"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY est un type utilisé pour définir un tableau de correctifs MIDI.


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

Chaque élément du tableau correspond à un correctif avec chacun des 16 bits représentant l’un des 16 canaux MIDI. Les bits sont définis pour chacun des canaux qui utilisent ce correctif particulier. Par exemple, si le correctif numéro 0 est utilisé par les canaux MIDI physiques 0 et 8, l’élément 0 du tableau doit être défini sur 0x0101.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| Version<br/>                  | MIDI (Musical Instrument Digital Interface), types MIDI<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Mmsystem. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types MIDI](midi-event-types.md)
</dt> </dl>

 

 





