---
description: L’interface ID3D10EffectVariable dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Spécialisation des interfaces (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514941"
---
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="77890-103">Spécialisation des interfaces (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="77890-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="77890-104">L' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="77890-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="77890-105">Les méthodes se présentent sous la forme *type* et incluent une méthode pour chaque type de variable d’effet (tel que AsBlend, AsConstantBuffer, etc.).</span><span class="sxs-lookup"><span data-stu-id="77890-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="77890-106">Par exemple, supposons que vous ayez un effet avec deux variables globales : Time et une transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="77890-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="77890-107">Voici un exemple (à partir de l' [exemple SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) qui obtient ces variables :</span><span class="sxs-lookup"><span data-stu-id="77890-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="77890-108">En spécialisant les interfaces, vous pouvez réduire le code à un seul appel.</span><span class="sxs-lookup"><span data-stu-id="77890-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="77890-109">Les interfaces qui héritent de l' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) ont également ces méthodes, mais elles ont été conçues pour retourner des objets non valides ; Seuls les appels de l' **interface ID3D10EffectVariable** retournent des objets valides.</span><span class="sxs-lookup"><span data-stu-id="77890-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="77890-110">Les applications peuvent tester l’objet retourné pour voir s’il est valide en appelant [**ID3D10EffectVariable :: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span><span class="sxs-lookup"><span data-stu-id="77890-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77890-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77890-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77890-112">Effets</span><span class="sxs-lookup"><span data-stu-id="77890-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



