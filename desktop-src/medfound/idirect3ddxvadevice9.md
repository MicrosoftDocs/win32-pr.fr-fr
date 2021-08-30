---
description: Représente un accélérateur matériel pour DirectX Video Acceleration (DXVA) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interface IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: c210492de77daffe6f67056ccc888aff49e950a16f0440010f46a2c5136a0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958219"
---
# <a name="idirect3ddxvadevice9-interface"></a>Interface IDirect3DDXVADevice9

Représente un accélérateur matériel pour DirectX Video Acceleration (DXVA) 1,0.

## <a name="members"></a>Membres

L’interface **IDirect3DDXVADevice9** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDirect3DDXVADevice9** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDirect3DDXVADevice9** possède ces méthodes.



| Méthode                                                  | Description                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [**BeginFrame**](idirect3ddxvadevice9-beginframe.md)   | Commence le traitement pour créer une image décodée.<br/>         |
| [**EndFrame**](idirect3ddxvadevice9-endframe.md)       | Termine le traitement pour créer une image décodée.<br/>           |
| [**Effectue**](idirect3ddxvadevice9-execute.md)         | Effectue une opération de décodage DXVA. <br/>                       |
| [**QueryStatus**](idirect3ddxvadevice9-querystatus.md) | Interroge l’État lecture/écriture d’une surface de décodage DXVA. <br/> |



 

## <a name="remarks"></a>Remarques

Pour obtenir un pointeur vers cette interface, appelez [**IDirect3DVideoDevice9 :: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces vidéo Direct3D](direct3d-video-interfaces.md)
</dt> </dl>

 

 
