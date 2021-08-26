---
description: Représente un pilote d’imprimante dont dépendent d’autres pilotes d’imprimante.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Structure CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 18ac3dba88d9cf781393b01b6594777426b7195e6f68afa0fd00a5bddb01f129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950399"
---
# <a name="core_printer_driver-structure"></a>Structure du pilote d' \_ imprimante principale \_

Représente un pilote d’imprimante dont dépendent d’autres pilotes d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a>Membres

<dl> <dt>

**CoreDriverGUID**
</dt> <dd>

GUID du pilote d’imprimante principal.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Date et heure de la dernière version du pilote d’imprimante principal.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

ID de version de la dernière version du pilote d’imprimante principal.

</dd> <dt>

**szPackageID \[ \_ chemin d’accès maximal\]**
</dt> <dd>

Chemin d’accès au package de pilotes qui contient le pilote d’imprimante principal.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure peut représenter le pilote de base d’un fabricant sur lequel les pilotes de différents modèles d’imprimante sont dépendants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ Core \_ Printer \_ DRIVERW** (Unicode) and **\_ Core \_ Printer \_ drivera** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




