---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 8864c298-be9a-4ff4-a9c5-996b62937c18
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 080e3a5692085286150aff3e072889b42a059ce6ccd8dea11807f781e4a004bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880111"
---
# <a name="d3dauthenticatedchannel_queryoutputid_input-structure"></a>\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID

Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DeviceHandle;
  HANDLE                              CryptoSessionHandle;
  UINT                                OutputIDIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_INPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Input**
</dt> <dd>

Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.

</dd> <dt>

**DeviceHandle**
</dt> <dd>

Handle de l’appareil.

</dd> <dt>

**CryptoSessionHandle**
</dt> <dd>

Handle de la session de chiffrement.

</dd> <dt>

**OutputIDIndex**
</dt> <dd>

Index de l’ID de sortie.

</dd> </dl>

## <a name="requirements"></a>Conditions requises



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

 

 




