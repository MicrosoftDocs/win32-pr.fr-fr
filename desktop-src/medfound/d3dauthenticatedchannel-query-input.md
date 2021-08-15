---
description: 'Contient des données d’entrée pour la méthode IDirect3DAuthenticatedChannel9 :: Query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Structure D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 50f9c781ca6d495acd06d3aa67c337dee76b2310f5399615599a52e15000382c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974687"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a>\_ \_ Structure d’entrée de la requête D3DAUTHENTICATEDCHANNEL

Contient des données d’entrée pour la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**Affectée**
</dt> <dd>

GUID qui spécifie la requête. Pour obtenir la liste des valeurs, consultez [protection du contenu des requêtes](content-protection-queries.md).

</dd> <dt>

**TRAITÉE**
</dt> <dd>

Handle vers le canal authentifié. Pour récupérer le handle, appelez [**IDirect3DDevice9Video :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**UINT**
</dt> <dd>

Numéro de séquence de la requête. Au début de la session, générez un nombre aléatoire 32 bits sécurisé par chiffrement à utiliser comme numéro de séquence de départ. Pour chaque requête, incrémentez le numéro de séquence de 1.

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

 

 




