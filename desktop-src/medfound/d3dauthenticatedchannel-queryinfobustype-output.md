---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY ACCESSIBILITYATTRIBUTES.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1f4d7a0f8ceadc4e40ceaf327b7dc45fd10bd3427620971b16c5a02659c0a067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828709"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a>\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYINFOBUSTYPE

Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Sortie**
</dt> <dd>

Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.

</dd> <dt>

**BusType**
</dt> <dd>

**Or au niveau du** bit des indicateurs de l’énumération [**D3DBUSTYPE**](d3dbustype.md) .

</dd> <dt>

**bAccessibleInContiguousBlocks**
</dt> <dd>

Si la **valeur est true**, les blocs contigus de mémoire vidéo peuvent être accessibles au processeur ou au bus.

</dd> <dt>

**bAccessibleInNonContiguousBlocks**
</dt> <dd>

Si la **valeur est true**, les blocs de mémoire vidéo non contigus peuvent être accessibles à l’UC ou au bus.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




