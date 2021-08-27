---
description: Représente les options de l’imprimante.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Structure PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d7eb7be8443c6a49c670e0573a79831a7aacfd88087f6ab19de632223b8588c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091749"
---
# <a name="printer_options-structure"></a>Structure des options de l’imprimante \_

Représente les options de l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille de la structure **des \_ options** de l’imprimante.

</dd> <dt>

**dwFlags**
</dt> <dd>

Ensemble d' [**indicateurs d' \_ option \_ d’imprimante**](printer-option-flags.md) qui spécifie comment le handle d’une imprimante retournée par [**OpenPrinter2**](openprinter2.md) sera utilisé par d’autres fonctions.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**\_indicateurs d’option d’imprimante \_**](printer-option-flags.md)
</dt> </dl>

 

 




