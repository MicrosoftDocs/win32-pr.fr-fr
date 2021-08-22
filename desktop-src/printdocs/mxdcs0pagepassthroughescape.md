---
description: La \_ structure MXDC S0PAGE \_ passthrough \_ Escape \_ t est une \_ structure d' \_ en-tête d’échappement MXDC \_ concaténée avec une \_ structure MXDC S0PAGE \_ Data \_ T.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Structure MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: f8e0a46766f38aec16758a1efc9c0cbc775c2131b1279dcc47f92ed41e77c0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099053"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>\_Structure MXDC S0PAGE \_ passthrough- \_ Escape \_

La structure **MXDC \_ S0PAGE \_ passthrough \_ Escape \_ t** est une structure d' [**\_ \_ en-tête d’échappement MXDC \_**](mxdcescapeheader.md) concaténée avec une structure [**MXDC \_ S0PAGE \_ Data \_ T**](mxdcs0pagedata.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Une [**structure \_ \_ \_ T d’en-tête d’échappement MXDC**](mxdcescapeheader.md) avec son membre **opcode** défini sur **MXDCOP \_ Set \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Structure [**MxdcS0PageData**](mxdcs0pagedata.md) qui représente une page de document XPS.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est transmise dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quand elle est appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) et que le membre **opcode** de la structure T de l' [**\_ \_ en-tête \_ d’échappement MXDC**](mxdcescapeheader.md) est **MXDCOP \_ défini \_ S0PAGE**. En conséquence, Microsoft XML document Converter (MXDC) transmet la page à l’imprimante sans la traiter.

Allouez de la mémoire pour l’échappement comme indiqué ci-dessous, définissez les champs en fonction des besoins, puis appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

L’application appelante est chargée de valider le code XML de la page de document XPS.

La consommation de streaming est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ définir la \_ \_ ressource S0PAGE** comme **opcode** pour chaque ressource sur la page avant de l’appeler avec **MXDCOP \_ définir \_ S0PAGE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
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

 

