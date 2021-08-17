---
description: La structure de la \_ ressource MXDC XPS \_ S0PAGE \_ contient des \_ informations sur une ressource, telle qu’une image ou une police, qui est associée à une page de document XPS et doit être transmise au fichier de sortie Microsoft XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Structure MXDC_XPS_S0PAGE_RESOURCE_T (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 21035a99b6237c481a5b7560f469086ef2960d655ba32582ed273edb48910ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971178"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>\_Structure de \_ la \_ ressource \_ T MXDC XPS S0PAGE

La structure de la **\_ ressource MXDC XPS \_ S0PAGE \_ \_** contient des informations sur une ressource, telle qu’une image ou une police, qui est associée à une page de document XPS et doit être transmise au fichier de sortie Microsoft XPS Document Converter (MXDC).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Taille totale de cette structure et de la ressource à laquelle elle pointe.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Une valeur de type [**MXDC \_ S0 \_ page \_ enums**](mxdcs0pageenums.md) indiquant le type de ressource, par exemple image TIFF ou police TrueType.

</dd> <dt>

**szUri**
</dt> <dd>

URI de la ressource. Ce nombre ne peut pas dépasser 260 octets.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Taille de la ressource en octets.

</dd> <dt>

**bData**
</dt> <dd>

Données de la ressource dans un tableau d’octets de taille 1 + taille de la ressource.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est ajoutée à une structure [**\_ t d' \_ en \_ -tête d’échappement MXDC**](mxdcescapeheader.md) (dont le **opcode** a la valeur **MXDCOP \_ Set \_ S0PAGERESOURCE**) pour créer une structure d' [**échappement de \_ \_ ressource \_ \_ MXDC S0PAGE**](mxdcs0pageresourceescape.md) . La structure **MXDC \_ S0PAGE \_ Resource \_ Escape \_ T** qui en résulte est ensuite transmise dans le paramètre *lpszInData* de la fonction [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) appelée avec l’échappement d' [**\_ échappement MXDC**](mxdc-escape.md) . L’effet est d’envoyer la ressource à MXDC pour la convertir et d’être écrite dans le fichier de sortie.

L’appel à [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) doit être compris entre un appel à [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) et un appel à [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Toutefois, il peut y avoir plusieurs appels de ce type entre les appels à **StartPage** et **EndPage**.

La consommation de la diffusion en continu est plus efficace si vous appelez [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) avec **MXDCOP \_ défini \_ S0PAGE \_** **opcode** de ressource pour chaque ressource sur la page avant d’appeler **ExtEscape** avec l' **opcode** **MXDCOP \_ Set \_ S0PAGE** .

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

 

