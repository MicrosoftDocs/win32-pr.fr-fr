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
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521887"
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

## <a name="remarks"></a>Notes

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

 

