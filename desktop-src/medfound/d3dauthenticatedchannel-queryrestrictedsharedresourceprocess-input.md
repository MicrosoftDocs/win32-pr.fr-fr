---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413053"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a>\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS

Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Input**
</dt> <dd>

Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.

</dd> <dt>

**ProcessIndex**
</dt> <dd>

Index du processus.

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 

 




