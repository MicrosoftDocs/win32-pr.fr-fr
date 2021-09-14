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
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118033"
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

## <a name="remarks"></a>Notes

Cette structure peut représenter le pilote de base d’un fabricant sur lequel les pilotes de différents modèles d’imprimante sont dépendants.

## <a name="requirements"></a>Spécifications



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

 

 




