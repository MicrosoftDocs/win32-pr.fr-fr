---
title: Registre des couleurs
description: Ces registres de sortie du nuanceur de sommets contiennent une valeur de couleur.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104321325"
---
# <a name="color-register"></a><span data-ttu-id="f0670-103">Registre des couleurs</span><span class="sxs-lookup"><span data-stu-id="f0670-103">Color Register</span></span>

<span data-ttu-id="f0670-104">Ces registres de sortie du nuanceur de sommets contiennent une valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="f0670-104">These vertex shader output registers contain a color value.</span></span> 

| <span data-ttu-id="f0670-105">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="f0670-105">Register</span></span> | <span data-ttu-id="f0670-106">Description</span><span class="sxs-lookup"><span data-stu-id="f0670-106">Description</span></span>              |
|----------|--------------------------|
| <span data-ttu-id="f0670-107">oD0</span><span class="sxs-lookup"><span data-stu-id="f0670-107">oD0</span></span>      | <span data-ttu-id="f0670-108">Registre des couleurs diffuses.</span><span class="sxs-lookup"><span data-stu-id="f0670-108">diffuse color register.</span></span>  |
| <span data-ttu-id="f0670-109">oD1</span><span class="sxs-lookup"><span data-stu-id="f0670-109">oD1</span></span>      | <span data-ttu-id="f0670-110">Registre de couleurs spéculaire.</span><span class="sxs-lookup"><span data-stu-id="f0670-110">specular color register.</span></span> |



 

<span data-ttu-id="f0670-111">La valeur oD0 est interpolée et écrite dans le registre de couleurs du nuanceur de pixels 0 (v0).</span><span class="sxs-lookup"><span data-stu-id="f0670-111">The oD0 value is interpolated and is written to the pixel shader color register 0 (v0).</span></span> <span data-ttu-id="f0670-112">La valeur oD1 est interpolée et écrite dans le registre de couleurs du nuanceur de pixels 1 (v1).</span><span class="sxs-lookup"><span data-stu-id="f0670-112">The oD1 value is interpolated and written to the pixel shader color register 1 (v1).</span></span> <span data-ttu-id="f0670-113">Pour plus d’informations sur les registres de couleurs du nuanceur de pixels, consultez la rubrique du [Registre des couleurs d’entrée](dx9-graphics-reference-asm-ps-registers-input-color.md) de nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="f0670-113">For more information about pixel shader color registers, see the pixel shader [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0670-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f0670-114">Remarks</span></span>

<span data-ttu-id="f0670-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="f0670-115">Example</span></span>


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a><span data-ttu-id="f0670-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0670-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0670-117">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="f0670-117">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




