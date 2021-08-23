---
description: La \_ structure MXDC S0PAGE \_ Data \_ T contient une page de document XPS à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Structure MXDC_S0PAGE_DATA_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 1ff54325859acef6da136c4bce20286bc7c746d8880d8994ca834213adf57b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776549"
---
# <a name="mxdc_s0page_data_t-structure"></a>\_Structure MXDC S0PAGE \_ Data \_ T

La structure **MXDC \_ S0PAGE \_ Data \_ T** contient une page de document XPS à transmettre au fichier de sortie Microsoft XPS Document Converter (MXDC) sans aucun traitement.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Taille de la mémoire tampon de sortie, **bData**.

</dd> <dt>

**bData**
</dt> <dd>

Page de document XPS.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est ajoutée à une structure [**\_ t d' \_ en \_ -tête d’échappement MXDC**](mxdcescapeheader.md) (dont le **opcode** a la valeur MXDCOP \_ Set \_ S0PAGE) pour créer une structure [**MXDC \_ S0PAGE passthrough d' \_ \_ échappement \_**](mxdcs0pagepassthroughescape.md) . Cette structure est ensuite transmise au paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quand elle est appelée avec [**MXDC \_ Escape**](mxdc-escape.md) comme caractère d’échappement. Le résultat est que le MXDC transmet la page à la sortie sans la traiter.

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

 

