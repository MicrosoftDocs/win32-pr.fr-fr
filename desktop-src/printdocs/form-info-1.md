---
description: La structure FORM_INFO_1 contient des informations sur un formulaire d’impression. Les informations incluent l’origine des formulaires imprimés, son nom, ses dimensions et les dimensions de sa zone imprimable.
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: Structure FORM_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 516f646d664a034f81a76eb2262b3ea8c950a87e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529272"
---
# <a name="form_info_1-structure"></a>Structure FORM_INFO_1

La structure **FORM_INFO_1** contient des informations sur un formulaire d’impression. Les informations incluent l’origine du formulaire d’impression, son nom, ses dimensions et les dimensions de sa zone imprimable.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**Indicateurs**
</dt> <dd>

Propriétés du formulaire. Les valeurs suivantes sont définies.



| Valeur         | Signification                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | Si cet indicateur de bit est défini, le formulaire a été défini par l’utilisateur. Les formulaires avec cet indicateur défini sont définis dans le registre.        |
| FORM_BUILTIN | Si cet indicateur de bit est défini, le formulaire fait partie du spouleur. Les définitions de formulaire pour lesquelles cet indicateur est défini n’apparaissent pas dans le registre. |
| FORM_PRINTER | Si cet indicateur de bit est défini, le formulaire est associé à une certaine imprimante et sa définition apparaît dans le registre.          |



 

</dd> <dt>

**pName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire. Le nom du formulaire ne peut pas dépasser 31 caractères.

</dd> <dt>

**Taille**
</dt> <dd>

Largeur et hauteur, en millièmes de millimètres, du formulaire.

</dd> <dt>

**ImageableArea**
</dt> <dd>

Largeur et hauteur, en millièmes de millimètres, du formulaire.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **_FORM_INFO_1W** (Unicode) et **_FORM_INFO_1A** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




