---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861805"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a>\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID

Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.

</dd> <dt>

**EncryptionGuidIndex**
</dt> <dd>

Index du GUID de chiffrement.

</dd> <dt>

**EncryptionGuid**
</dt> <dd>

GUID qui spécifie un type de chiffrement pris en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




