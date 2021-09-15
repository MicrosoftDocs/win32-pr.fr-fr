---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY CHANNELTYPE.
ms.assetid: 547f7f26-2b9d-48b1-97cc-84a2202c3900
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3120669da69f13359f49d8b8c38ed7d3e211a8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413056"
---
# <a name="d3dauthenticatedchannel_querychanneltype_output-structure"></a>\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYCHANNELTYPE

Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DAUTHENTICATEDCHANNELTYPE          ChannelType;
} D3DAUTHENTICATEDCHANNEL_QUERYCHANNELTYPE_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Sortie**
</dt> <dd>

Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.

</dd> <dt>

**ChannelType**
</dt> <dd>

Valeur [**D3DAUTHENTICATEDCHANNELTYPE**](d3dauthenticatedchanneltype.md) qui spécifie le type de canal.

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

 

 




