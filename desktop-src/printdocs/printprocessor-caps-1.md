---
description: La \_ structure PRINTPROCESSOR Cap \_ 1 est le format des informations sur les fonctionnalités de l’imprimante qui est retournée par la fonction GetPrinterData dans le tampon spécifié par la variable pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Structure PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536810"
---
# <a name="printprocessor_caps_1-structure"></a>\_Structure PRINTPROCESSOR Cap \_ 1

La structure **PRINTPROCESSOR \_ Cap \_ 1** est le format des informations sur les fonctionnalités de l’imprimante qui est retournée par la fonction [**GetPrinterData**](getprinterdata.md) dans le tampon spécifié par la variable *pData* .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwLevel**
</dt> <dd>

Numéro de version de la structure. Cette valeur doit être 1.

</dd> <dt>

**dwNupOptions**
</dt> <dd>

Masque de bits représentant les différents nombres de pages de document que l’imprimante peut imprimer sur une page physique. Le bit le moins significatif représente 1 page de document par page, le bit suivant représente 2 pages de document par page, et ainsi de suite. Par exemple, 0x0000810B indique que l’imprimante prend en charge les pages de documents 1, 2, 4, 9 et 16 par page physique.

</dd> <dt>

**dwPageOrderFlags**
</dt> <dd>

Ordre dans lequel les pages seront imprimées. Cette valeur peut être \_ impression normale, INverser l' \_ impression ou livret \_ imprimé.

</dd> <dt>

**dwNumberOfCopies**
</dt> <dd>

Nombre maximal de copies que l’imprimante peut gérer.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs de tous les membres de structure sont fournies par la fonction [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , qui est documentée dans le kit WDK (Windows Driver Kit).

Le spouleur appelle la fonction [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) d’un processeur d’impression lorsqu’une application appelle [**GetPrinterData**](getprinterdata.md), en spécifiant un nom de valeur au format PrintProcCaps \_ *DataType*, où *DataType* est le nom d’un type de données d’entrée.

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

[**GetPrinterData**](getprinterdata.md)
</dt> </dl>

 

