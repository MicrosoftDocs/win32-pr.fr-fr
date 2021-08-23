---
description: La \_ structure doc info \_ 2 décrit un document qui sera imprimé.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Structure DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 27d7753fa16abcfbc30b28bcc4343b2e1ef7996cad408b54fefb850feac9b17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846259"
---
# <a name="doc_info_2-structure"></a>\_Structure infos doc \_ 2

La structure **doc \_ info \_ 2** décrit un document qui sera imprimé.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
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

**dwMode**
</dt> <dd>

Informe le spouleur d’impression de la nature des données à suivre. Si cette valeur est égale à zéro, le spouleur d’impression traite les données envoyées par les appels suivants à [**WritePrinter**](writeprinter.md) en tant que travail d’impression normal (qu’ils soient ou non mis en file d’attente dépend de la propriété Printer). Si cette valeur est DI \_ Channel, seul un canal de communication est ouvert. Dans ce cas, les données passées dans les appels suivants à **WritePrinter** sont envoyées à l’imprimante ou les appels suivants à [**ReadPrinter**](readprinter.md) récupèrent les données de l’imprimante. Ce mode reste effectif jusqu’à l’appel de [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .

</dd> <dt>

**JobId**
</dt> <dd>

Réservé à un usage interne ; doit être égal à zéro.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **\_ \_ Infos doc \_ 2S** (Unicode) et **\_ \_ infos doc \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




