---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY OUTPUTID.
ms.assetid: 4dfd1d65-b203-456a-bc9b-527906bcf87e
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYROUTPUTID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 26686126fd2a5cb942c88ea485f753d2432499dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530856"
---
# <a name="d3dauthenticatedchannel_queryroutputid_output-structure"></a>\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYROUTPUTID

Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  HANDLE DeviceHandle;
  HANDLE CryptoSessionHandle;
  UINT   OutputIDIndex;
  UINT64 OutputID;
} D3DAUTHENTICATEDCHANNEL_QUERYOUTPUTID_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.

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

Index de l’ID de sortie donné dans le membre **OutputID** .

</dd> <dt>

**OutputID**
</dt> <dd>

ID de sortie associé à l’appareil et à la session de chiffrement spécifiés.

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

 

 




