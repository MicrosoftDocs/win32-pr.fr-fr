---
description: Valeurs de largeur, de hauteur et de profondeur de la structure D3D12_DISPATCH_RAYS_DESC spécifiée dans l’appel DispatchRays d’origine.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514367"
---
# <a name="dispatchraysdimensions"></a><span data-ttu-id="d25bb-103">DispatchRaysDimensions</span><span class="sxs-lookup"><span data-stu-id="d25bb-103">DispatchRaysDimensions</span></span>

<span data-ttu-id="d25bb-104">Valeurs de largeur, de hauteur et de profondeur de la structure **\_ \_ \_ desc des rayons D3D12 Dispatch** spécifiés dans l’appel [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) d’origine.</span><span class="sxs-lookup"><span data-stu-id="d25bb-104">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d25bb-105">Syntax</span></span>

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a><span data-ttu-id="d25bb-106">Notes</span><span class="sxs-lookup"><span data-stu-id="d25bb-106">Remarks</span></span>

<span data-ttu-id="d25bb-107">Cette fonction peut être appelée à partir des types de nuanceur Raytracing suivants :</span><span class="sxs-lookup"><span data-stu-id="d25bb-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="d25bb-108">**Tout nuanceur de correspondance**</span><span class="sxs-lookup"><span data-stu-id="d25bb-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="d25bb-109">**Nuanceur pouvant être appelé**</span><span class="sxs-lookup"><span data-stu-id="d25bb-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="d25bb-110">**Nuanceur de correspondance le plus proche**</span><span class="sxs-lookup"><span data-stu-id="d25bb-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="d25bb-111">**Nuanceur d’intersection**</span><span class="sxs-lookup"><span data-stu-id="d25bb-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="d25bb-112">**Nuanceur manque**</span><span class="sxs-lookup"><span data-stu-id="d25bb-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="d25bb-113">**Nuanceur de création de rayon**</span><span class="sxs-lookup"><span data-stu-id="d25bb-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="d25bb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d25bb-114">See also</span></span>

* [<span data-ttu-id="d25bb-115">Référence HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="d25bb-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
