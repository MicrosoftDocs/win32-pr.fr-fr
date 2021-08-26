---
description: La \_ structure doc info \_ 1 décrit un document qui sera imprimé.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Structure DOC_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: f534031da1c8f8f50309d4a2db0bfa39fe272ac34f59d1b490c24026d8fee261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949999"
---
# <a name="doc_info_1-structure"></a>\_Structure infos doc \_ 1

La structure **doc \_ info \_ 1** décrit un document qui sera imprimé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a>Membres

<dl> <dt>

**pDocName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du document.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un fichier de sortie. Pour imprimer sur une imprimante, affectez-lui la valeur **null**.

</dd> <dt>

**pDatatype**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer le document.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos doc \_ 1s** (Unicode) et **\_ \_ infos doc \_ 1a** (ANSI)<br/>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




