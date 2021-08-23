---
description: La \_ structure SYSTEMTIME nommée définit une étiquette qui s’affiche lorsqu’une valeur de propriété SYSTEMTIME spécifique est détectée.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Structure de LABELED_SYSTEMTIME (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 94ce2a2e0b86c24ea6c16627fd0b866e18aaf48f3c1f0b318a601809e1ee03dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742709"
---
# <a name="labeled_systemtime-structure"></a>\_Structure SYSTEMTIME étiquetée

La **structure \_ SystemTime nommée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété SYSTEMTIME spécifique est détectée.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a>Membres

<dl> <dt>

**Valeur**
</dt> <dd>

Valeur SYSTEMTIME d’une propriété que vous souhaitez détecter.

</dd> <dt>

**Étiquette**
</dt> <dd>

Description textuelle ou étiquette qui s’affiche lorsque la valeur SYSTEMTIME spécifiée dans le membre de **valeur** est détectée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le membre **lpLabeledSystemTimeTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent une ou plusieurs paires de valeurs d’étiquette. Les paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur LARGEINT spécifique trouvée dans le paquet de protocole.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




