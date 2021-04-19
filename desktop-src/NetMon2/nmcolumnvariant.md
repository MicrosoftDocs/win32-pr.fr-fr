---
description: Fournit une ligne dans le volet supérieur de la observateur d’événements qui sert de conteneur pour toutes les données possibles insérées dans une colonne.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: NMCOLUMNVARIANT, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522001"
---
# <a name="nmcolumnvariant-structure"></a>NMCOLUMNVARIANT, structure

La structure **NMCOLUMNVARIANT** fournit une ligne dans le volet supérieur de la observateur d’événements qui sert de conteneur pour toutes les données possibles insérées dans une colonne.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Type**
</dt> <dd>

Valeur du type d’énumération [**NMCOLUMNTYPE**](nmcolumntype.md) .

</dd> <dt>

**Valeur**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

valeur de l’entier non signé 8 bits.

</dd> <dt>

**Sint8Val**
</dt> <dd>

valeur de l’entier signé 8 bits.

</dd> <dt>

**Uint16Val**
</dt> <dd>

valeur de l’entier non signé 16 bits.

</dd> <dt>

**Sint16Val**
</dt> <dd>

valeur de l’entier signé 16 bits.

</dd> <dt>

**Uint32Val**
</dt> <dd>

valeur de l’entier non signé 32 bits.

</dd> <dt>

**Sint32Val**
</dt> <dd>

valeur de l’entier signé 32 bits.

</dd> <dt>

**Float64Val**
</dt> <dd>

valeur flottante 64 bits.

</dd> <dt>

**FrameVal**
</dt> <dd>

Numéro de frame.

</dd> <dt>

**YesNoVal**
</dt> <dd>

Affiche Oui ou non.

</dd> <dt>

**OnOffVal**
</dt> <dd>

Affiche activé ou désactivé.

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

Affiche true ou false.

</dd> <dt>

**MACAddrVal**
</dt> <dd>

Adresse MAC.

</dd> <dt>

**IPXAddrVal**
</dt> <dd>

Adresse IPX.

</dd> <dt>

**IPAddrVal**
</dt> <dd>

Adresse IP.

</dd> <dt>

**VarTimeVal**
</dt> <dd>

Heure de la variante. Utilisez **VariantTimetoSystemTime** pour effectuer la conversion en heure système.

</dd> <dt>

**pStringVal**
</dt> <dd>

Pointeur vers une chaîne.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




