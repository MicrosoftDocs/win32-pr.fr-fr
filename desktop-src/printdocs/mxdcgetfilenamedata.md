---
description: La \_ structure MXDC \_ obtenir \_ \_ des données de nom de fichier contient le chemin d’accès complet et le nom de fichier d’un fichier de sortie Microsoft XPS Document Converter (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Structure MXDC_GET_FILENAME_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864962"
---
# <a name="mxdc_get_filename_data_t-structure"></a>MXDC de l’accès à la \_ \_ structure des données de nom de fichier \_ \_

La structure **MXDC \_ obtenir des \_ \_ données de \_ nom** de fichier contient le chemin d’accès complet et le nom de fichier d’un fichier de sortie Microsoft XPS Document Converter (MXDC).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbOutput**
</dt> <dd>

Taille de la mémoire tampon de sortie, **wszData**.

</dd> <dt>

**wszData**
</dt> <dd>

Chemin d’accès complet et nom de fichier du fichier de sortie.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est retournée par [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) lorsqu’elle est appelée avec l’échappement d’échappement [**MXDC \_**](mxdc-escape.md) et que la structure [**\_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) qui est passée dans le paramètre *lpszInData* a son **opcode** défini sur **MXDCOP recevoir le \_ nom de \_ fichier**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Structures de l’API du spouleur d’impression](printing-and-print-spooler-structures.md)
</dt> <dt>

[Fonctions d’échappement d’imprimante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ échappement**](mxdc-escape.md)
</dt> </dl>

 

