---
description: Spécifie le type de canal authentifié Direct3D.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Énumération D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196815"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a>Énumération D3DAUTHENTICATEDCHANNELTYPE

Spécifie le type de canal authentifié Direct3D.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ d3d9**
</dt> <dd>

Canal Direct3D 9. Ce canal fournit la communication avec le runtime Direct3D.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Canal du pilote de logiciel. Ce canal fournit une communication avec un pilote qui implémente des mécanismes de protection de contenu dans le logiciel.

</dd> <dt>

<span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**
</dt> <dd>

Canal du pilote matériel. Ce canal fournit une communication avec un pilote qui implémente des mécanismes de protection du contenu dans le matériel GPU.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>D3d9types. h (inclure d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de vidéos Direct3D](direct3d-video-enumerations.md)
</dt> <dt>

[**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




