---
description: La \_ structure d’informations sur l’imprimante \_ 8 spécifie les paramètres globaux de l’imprimante par défaut.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Structure PRINTER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0aa5d516dd099caeba5699a8328fa52add64f14ea970e6ccec28ea8bfbe87271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947669"
---
# <a name="printer_info_8-structure"></a>\_Structure des informations sur l’imprimante \_ 8

La structure d' **\_ informations sur l’imprimante \_ 8** spécifie les paramètres globaux de l’imprimante par défaut.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a>Membres

<dl> <dt>

**pDevMode**
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui définit les données globales de l’imprimante par défaut, telles que l’orientation du papier et la résolution.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les paramètres globaux par défaut sont définis par l’administrateur d’une imprimante qui peut être utilisée par n’importe qui. En revanche, les valeurs par défaut par utilisateur affectent un utilisateur particulier ou toute autre personne qui utilise le profil. Pour les valeurs par défaut par utilisateur, utilisez [**Printer \_ info \_ 9**](printer-info-9.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos sur \_ l’imprimante 8W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 8A** (ANSI)<br/>                           |



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

[**\_Infos sur l’imprimante \_ 9**](printer-info-9.md)
</dt> </dl>

 

 




