---
title: Spécialisation des interfaces (Direct3D 11)
description: ID3DX11EffectVariable dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674246"
---
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="e2a22-103">Spécialisation des interfaces (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e2a22-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="e2a22-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="e2a22-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="e2a22-105">Les méthodes se présentent sous la forme *AsType* et incluent une méthode pour chaque type de variable d’effet (tel que AsBlend, AsConstantBuffer, etc.).</span><span class="sxs-lookup"><span data-stu-id="e2a22-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="e2a22-106">Par exemple, supposons que vous ayez un effet avec deux variables globales : Time et une transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="e2a22-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="e2a22-107">Voici un exemple qui obtient ces variables :</span><span class="sxs-lookup"><span data-stu-id="e2a22-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="e2a22-108">En spécialisant les interfaces, vous pouvez réduire le code à un seul appel.</span><span class="sxs-lookup"><span data-stu-id="e2a22-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="e2a22-109">Les interfaces qui héritent de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) ont également ces méthodes, mais elles ont été conçues pour retourner des objets non valides ; Seuls les appels de **ID3DX11EffectVariable** retournent des objets valides.</span><span class="sxs-lookup"><span data-stu-id="e2a22-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="e2a22-110">Les applications peuvent tester l’objet retourné pour voir s’il est valide en appelant [**ID3DX11EffectVariable :: IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="e2a22-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2a22-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2a22-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2a22-112">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e2a22-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




