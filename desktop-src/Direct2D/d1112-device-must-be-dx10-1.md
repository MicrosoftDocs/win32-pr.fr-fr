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
ms.openlocfilehash: b4204e04332876db9145baba9888dbb2d339eff9
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104030950"
---
# <a name="d1112-device-must-be-dx11"></a><span data-ttu-id="68c07-104">D1112 : l’appareil doit être DX11</span><span class="sxs-lookup"><span data-stu-id="68c07-104">D1112: Device Must Be DX11</span></span>

<span data-ttu-id="68c07-105">L’appareil associé à la surface DXGI doit être un appareil D3D11.</span><span class="sxs-lookup"><span data-stu-id="68c07-105">The device associated with the DXGI surface must be a D3D11 device.</span></span>



|             |         |
|-------------|---------|
| <span data-ttu-id="68c07-106">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="68c07-106">Error Level</span></span> | <span data-ttu-id="68c07-107">Avertissement</span><span class="sxs-lookup"><span data-stu-id="68c07-107">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="68c07-108">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="68c07-108">Possible Causes</span></span>

<span data-ttu-id="68c07-109">Une tentative d’utilisation de [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) avec une surface DXGI créée par un appareil non Direct3D11 a été tentée.</span><span class="sxs-lookup"><span data-stu-id="68c07-109">There was an attempt to use the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) with a DXGI surface created by a non-Direct3D11 device.</span></span>

 

 




