---
description: La \_ structure information \_ d’analyse 1 identifie un moniteur installé.
ms.assetid: 7a4660bd-5df8-49dd-92f6-9574f451f10d
title: Structure MONITOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_1
- _MONITOR_INFO_1A
- _MONITOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dff4fa4913be25d8a7cb5cd3324bd6e13d68761147fa76c451b587fb9569257d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099083"
---
# <a name="monitor_info_1-structure"></a>Structure d’information d’analyse \_ \_ 1

La **structure \_ information \_ d’analyse 1** identifie un moniteur installé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MONITOR_INFO_1 {
  LPTSTR pName;
} MONITOR_INFO_1, *PMONITOR_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie un moniteur installé.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ Analyser les \_ informations \_ 1s** (Unicode) et **\_ \_ informations sur le moniteur \_ 1a** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**\_Informations sur le moniteur \_ 2**](monitor-info-2.md)
</dt> </dl>

 

 




