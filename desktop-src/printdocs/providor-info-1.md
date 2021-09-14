---
description: La \_ structure PROVIDOR info \_ 1 identifie un fournisseur d’impression.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Structure PROVIDOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196691"
---
# <a name="providor_info_1-structure"></a>PROVIDOR \_ information \_ 1 (structure)

La structure **PROVIDOR \_ info \_ 1** identifie un fournisseur d’impression.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui est le nom du fournisseur d’impression.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Pointeur vers une chaîne d’environnement se terminant par un caractère null qui spécifie l’environnement dans lequel la bibliothèque de liens dynamiques (DLL) du fournisseur est conçue pour s’exécuter.

</dd> <dt>

**pDLLName**
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui est le nom du fournisseur .dll.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ PROVIDOR \_ info \_ 1s** (Unicode) et **\_ PROVIDOR \_ info \_ 1a** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




