---
description: La \_ structure information \_ d’analyse 2 identifie une analyse.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Structure MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c01377740c77ef4cb2be15e785b9ea3e93449944c11f2014ed660d8c3e3245b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112329"
---
# <a name="monitor_info_2-structure"></a>Structure du moniteur \_ informations \_ 2

La **structure \_ information \_ d’analyse 2** identifie une analyse.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui est le nom de l’analyse.

</dd> <dt>

**pEnvironment**
</dt> <dd>

pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement pour lequel le moniteur a été écrit (par exemple, Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui est le nom de la DLL de l’analyseur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ Analyser les \_ informations \_ 2S** (Unicode) et **\_ \_ informations sur le moniteur \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**\_Informations sur le moniteur \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




