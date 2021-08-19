---
description: La \_ structure Printer info \_ 3 spécifie les informations de sécurité de l’imprimante.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Structure PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6b9bc249921b3247f5df898c2810d735dc1a75c8e643e965b3fd249d9496f78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867924"
---
# <a name="printer_info_3-structure"></a>Structure de l’imprimante \_ info \_ 3

La structure **Printer \_ info \_ 3** spécifie les informations de sécurité de l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a>Membres

<dl> <dt>

**pSecurityDescriptor**
</dt> <dd>

Pointeur vers une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui spécifie les informations de sécurité d’une imprimante.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure **Printer \_ info \_ 3** permet à une application d’obtenir et de définir le descripteur de sécurité d’une imprimante. L’appelant peut le faire même s’il ne dispose pas d’autorisations d’imprimante spécifiques, à condition qu’il dispose des droits standard décrits dans [**SetPrinter**](setprinter.md) et [**GetPrinter**](getprinter.md). Par conséquent, une application peut refuser temporairement tout accès à une imprimante, tout en autorisant le propriétaire de l’imprimante à accéder à la liste de contrôle d’accès discrétionnaire de l’imprimante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 1**](printer-info-1.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 4**](printer-info-4.md)
</dt> <dt>

[**descripteur de sécurité \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

