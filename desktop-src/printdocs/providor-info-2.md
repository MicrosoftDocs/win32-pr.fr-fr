---
description: La \_ structure PROVIDOR info \_ 2 ajoute un fournisseur d’impression à la liste ordre des fournisseurs d’impression.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Structure PROVIDOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196687"
---
# <a name="providor_info_2-structure"></a>\_Structure PROVIDOR info \_ 2

La structure **PROVIDOR \_ info \_ 2** ajoute un fournisseur d’impression à la liste ordre des fournisseurs d’impression.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Membres

<dl> <dt>

**pOrder**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fournisseur d’impression.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée lors de l’appel de [**AddPrintProvidor**](addprintprovidor.md), niveau 2, pour ajouter le fournisseur d’impression spécifié à la fin de la liste des commandes du fournisseur d’impression. Le fournisseur est immédiatement utilisé pour le routage si l’appel a échoué.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ PROVIDOR \_ info \_ 2S** (Unicode) et **\_ PROVIDOR \_ info \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




