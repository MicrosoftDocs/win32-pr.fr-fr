---
description: La structure PATTERNMATCH définit les éléments de modèle utilisés pour évaluer un frame.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: PATTERNMATCH, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6bb92e2ae9a00c06e799c2e7378a40de09160e9bf94625e15a5a0e2091a5dae1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037059"
---
# <a name="patternmatch-structure"></a>PATTERNMATCH, structure

La structure **PATTERNMATCH** définit les éléments de modèle utilisés pour évaluer un frame.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a>Membres

<dl> <dt>

**Indicateurs**
</dt> <dd>

Indicateurs de correspondance de modèle :



| Valeur                                                                                                                                                                                                                                                                                           | Signification                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**Modèle \_ Indicateurs de correspondance \_ \_ non**</dt> <dt>0x00000001</dt> </dl>                                   | Lorsqu’il est défini, cet indicateur conserve les trames qui n’ont pas le modèle spécifié dans l’emplacement approprié.<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**Modèle \_ PORT des indicateurs de correspondance \_ \_ \_ spécifié**</dt> . <dt></dt> </dl> | Recherche une valeur de numéro de port.<br/>                                                             |



 

</dd> <dt>

**OffsetBasis**
</dt> <dd>

Types de décalage, qui peuvent être l’un des suivants :



| Valeur                                                                                                                                                                                                                                                       | Signification                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**\_base \_ de décalage par rapport \_ au \_ Frame**</dt> </dl>                                         | Définit un décalage, en octets, par rapport au début du frame.<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**DÉCALAGE \_ \_ de base par rapport \_ au \_ \_ protocole effectif**</dt> </dl> | Définit un décalage, en octets, par rapport au début du protocole référencé.<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**\_base \_ de décalage par rapport \_ à \_ IPX**</dt> </dl>                                               | Définit un décalage, en octets, uniquement par rapport à IPX.<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**\_base \_ de décalage par rapport \_ à l' \_ adresse IP**</dt> </dl>                                                  | Définit un décalage, en octets, uniquement par rapport à l’adresse IP.<br/>                              |



 

</dd> <dt>

**Port**
</dt> <dd>

Valeur de port, si elle est spécifiée.

</dd> <dt>

**Offset**
</dt> <dd>

Décalage, en octets, par rapport à **OffsetBasis**.

</dd> <dt>

**Durée**
</dt> <dd>

Longueur du modèle correspondant.

</dd> <dt>

**PatternToMatch**
</dt> <dd>

Modèle à faire correspondre.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est utilisée pour construire un filtre de capture. Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md).

Un filtre de capture peut contenir jusqu’à quatre structures **PATTERNMATCH** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




