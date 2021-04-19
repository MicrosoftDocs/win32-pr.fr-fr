---
description: La \_ structure des \_ valeurs d’énumération d’imprimante spécifie le nom, le type et les données de la valeur pour une valeur de configuration d’imprimante retournée par la fonction EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Structure PRINTER_ENUM_VALUES (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541837"
---
# <a name="printer_enum_values-structure"></a>\_Structure des valeurs d’énumération d’imprimante \_

La structure des **\_ \_ valeurs d’énumération d’imprimante** spécifie le nom, le type et les données de la valeur pour une valeur de configuration d’imprimante retournée par la fonction [**EnumPrinterDataEx**](enumprinterdataex.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>Membres

<dl> <dt>

**pValueName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de la valeur récupérée.

</dd> <dt>

**cbValueName**
</dt> <dd>

Nombre d’octets dans le membre **pValueName** , y compris le caractère null de fin.

</dd> <dt>

**dwType**
</dt> <dd>

Code indiquant le type de données vers lequel pointe le membre **pData** . Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Pointeur vers une mémoire tampon contenant les données de la valeur récupérée.

</dd> <dt>

**cbData**
</dt> <dd>

Nombre d’octets récupérés dans la mémoire tampon **pData** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ \_ VALUESW d’énumération d’imprimante** (Unicode) et **\_ \_ \_ valeurs d’énumération d’imprimante** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

