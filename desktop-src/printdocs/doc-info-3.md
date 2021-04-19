---
description: La \_ structure doc info \_ 3 décrit un document qui sera imprimé.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Structure DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524629"
---
# <a name="doc_info_3-structure"></a>\_Structure infos doc \_ 3

La structure **doc \_ info \_ 3** décrit un document qui sera imprimé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a>Membres

<dl> <dt>

**pDocName**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du document.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un fichier de sortie.

</dd> <dt>

**pDatatype**
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer le document.

</dd> <dt>

**dwFlags**
</dt> <dd>

Père. Actuellement, il peut s’agir de la **valeur null** ou de ce qui suit.



| Indicateur                 | Signification                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_écriture di MEMORYMAP \_ | Force [**StartDocPrinter**](startdocprinter.md) à ne pas utiliser [**AddJob**](addjob.md) et [**ScheduleJob**](schedulejob.md) pour l’impression locale. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Le \_ \_ paramètre d’écriture di MEMORYMAP dans **doc \_ info \_ 3** est une optimisation. Cela permet à GDI de mapper les fichiers de mise en file d’attente dans l’application et d’accélérer l’enregistrement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ Informations de document \_ \_ 3W** (Unicode) et **\_ \_ infos doc \_ 3A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




