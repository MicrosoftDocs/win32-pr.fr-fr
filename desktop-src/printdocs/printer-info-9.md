---
description: La \_ structure info 9 de l’imprimante \_ spécifie les paramètres par défaut de l’imprimante par utilisateur.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Structure PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545855"
---
# <a name="printer_info_9-structure"></a>\_Structure info 9 de l’imprimante \_

La **structure \_ info \_ 9** de l’imprimante spécifie les paramètres par défaut de l’imprimante par utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a>Membres

<dl> <dt>

**pDevMode**
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui définit les données d’imprimante par défaut par utilisateur, telles que l’orientation du papier et la résolution. Le **DEVMODE** est stocké dans le registre de l’utilisateur.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs par défaut par utilisateur affectent uniquement un utilisateur particulier ou toute personne qui utilise le profil. En revanche, les valeurs par défaut globales sont définies par l’administrateur d’une imprimante qui peut être utilisée par n’importe qui. Pour les valeurs par défaut globales, utilisez [**Printer \_ info \_ 8**](printer-info-8.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 9W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 9A** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 8**](printer-info-8.md)
</dt> </dl>

 

 




