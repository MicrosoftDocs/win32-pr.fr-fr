---
title: L’appareil D1112 doit être DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: L’appareil associé à la surface DXGI doit être un appareil D3D11.
keywords:
- L’appareil D1112 doit être DX11 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 24c8bf123d9e00eff90f216676ec03f7d68cbe692511118c36c1433cbf0354d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758109"
---
# <a name="d1112-device-must-be-dx11"></a>D1112 : l’appareil doit être DX11

L’appareil associé à la surface DXGI doit être un appareil D3D11.



| &nbsp;      |  &nbsp; |
|-------------|---------|
| Niveau d’erreur | Avertissement |



 

## <a name="possible-causes"></a>Causes possibles

Une tentative d’utilisation de [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) avec une surface DXGI créée par un appareil non Direct3D11 a été tentée.

 

 




