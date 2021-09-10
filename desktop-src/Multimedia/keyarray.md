---
title: Keyarray (mmsystem. h)
description: Keyarray spécifie un type utilisé pour définir un tableau de clés.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- MIDIPATCHSIZE DE TABLEAU
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364347"
---
# <a name="keyarray"></a>Tableau de la matrice

Keyarray spécifie un type utilisé pour définir un tableau de clés.


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**MIDIPATCHSIZE de tableau \[\]**
</dt> <dd>

Chaque élément du tableau correspond à un correctif à percussion basé sur des clés avec chacun des 16 bits représentant l’un des 16 canaux MIDI. Les bits sont définis pour chacun des canaux qui utilisent ce correctif particulier. Par exemple, si le correctif de percussion pour la clé numéro 60 est utilisé par les canaux MIDI physiques 9 et 15, l’élément 60 du tableau doit être défini sur 0x8200.

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

 

 





