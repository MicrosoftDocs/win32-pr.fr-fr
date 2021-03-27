---
title: Clonage d’un effet
description: Le clonage d’un effet crée une deuxième copie quasiment identique de l’effet.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674002"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="db7c8-103">Clonage d’un effet</span><span class="sxs-lookup"><span data-stu-id="db7c8-103">Cloning an Effect</span></span>

<span data-ttu-id="db7c8-104">Le clonage d’un effet crée une deuxième copie quasiment identique de l’effet.</span><span class="sxs-lookup"><span data-stu-id="db7c8-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="db7c8-105">Pour une explication de la raison pour laquelle il n’est pas exact, consultez le qualificateur unique suivant.</span><span class="sxs-lookup"><span data-stu-id="db7c8-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="db7c8-106">Une deuxième copie d’un effet est utile quand vous souhaitez utiliser l’infrastructure Effects sur plusieurs threads, puisque le runtime Effect n’est pas thread-safe pour maintenir des performances élevées.</span><span class="sxs-lookup"><span data-stu-id="db7c8-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="db7c8-107">Étant donné que les contextes de périphérique sont également non thread-sécurisés, différents threads doivent passer différents contextes de périphérique à la méthode ID3DX11EffectPass :: apply.</span><span class="sxs-lookup"><span data-stu-id="db7c8-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="db7c8-108">Un effet peut être cloné à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="db7c8-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="db7c8-109">Dans l’exemple ci-dessus, la copie clonée encapsule le même État que l’effet d’origine, quel que soit l’état d’origine de l’effet.</span><span class="sxs-lookup"><span data-stu-id="db7c8-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="db7c8-110">En particulier :</span><span class="sxs-lookup"><span data-stu-id="db7c8-110">In particular:</span></span>

1.  <span data-ttu-id="db7c8-111">Si pEffect est optimisé, l’effet pCloned est optimisé</span><span class="sxs-lookup"><span data-stu-id="db7c8-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="db7c8-112">Si pEffect a des variables gérées par l’utilisateur, pCloned Effect aura les mêmes variables gérées par l’utilisateur (voir la description unique ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="db7c8-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="db7c8-113">Toute mise à jour de variable en attente (jusqu’à ce qu’un appel de mise à jour de l’état de l’appareil) dans pEffect sera en attente dans pClonedEffect</span><span class="sxs-lookup"><span data-stu-id="db7c8-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="db7c8-114">Les objets d’appareil Direct3D 11 suivants sont immuables ou jamais mis à jour par l’infrastructure Effects, de sorte que l’effet cloné pointe vers les mêmes objets que l’effet d’origine :</span><span class="sxs-lookup"><span data-stu-id="db7c8-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="db7c8-115">Objets de bloc d’État (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span><span class="sxs-lookup"><span data-stu-id="db7c8-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="db7c8-116">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="db7c8-116">Shaders</span></span>
3.  <span data-ttu-id="db7c8-117">Instances de classe</span><span class="sxs-lookup"><span data-stu-id="db7c8-117">Class instances</span></span>
4.  <span data-ttu-id="db7c8-118">Textures (à l’exclusion des mémoires tampons de texture)</span><span class="sxs-lookup"><span data-stu-id="db7c8-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="db7c8-119">Vues d’accès non ordonnées</span><span class="sxs-lookup"><span data-stu-id="db7c8-119">Unordered access views</span></span>

<span data-ttu-id="db7c8-120">Les objets d’appareil Direct3D 11 suivants sont immuables et modifiés par le runtime Effect (sauf s’ils sont gérés par l’utilisateur ou uniques dans un effet cloné); de nouvelles copies de ces objets sont créées en cas de non-simple :</span><span class="sxs-lookup"><span data-stu-id="db7c8-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="db7c8-121">Mémoires tampons constantes</span><span class="sxs-lookup"><span data-stu-id="db7c8-121">Constant buffers</span></span>
2.  <span data-ttu-id="db7c8-122">Mémoires tampons de texture</span><span class="sxs-lookup"><span data-stu-id="db7c8-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="db7c8-123">Mémoires tampons à constante unique et mémoires tampons de texture</span><span class="sxs-lookup"><span data-stu-id="db7c8-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="db7c8-124">Notez que cette discussion s’applique à la fois aux mémoires tampons constantes et aux textures, mais que les mémoires tampons constantes sont prises en compte pour faciliter la lecture.</span><span class="sxs-lookup"><span data-stu-id="db7c8-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="db7c8-125">Il peut arriver qu’une mémoire tampon constante soit uniquement mise à jour par un thread, mais que l’état de l’appareil défini par les effets clonés utilise ces données.</span><span class="sxs-lookup"><span data-stu-id="db7c8-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="db7c8-126">Par exemple, l’effet principal peut mettre à jour les matrices universelles et de vue qui sont référencées à partir des nuanceurs dans des effets clonés qui ne modifient pas les matrices de monde et de vue.</span><span class="sxs-lookup"><span data-stu-id="db7c8-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="db7c8-127">Dans ces cas, les effets clonés doivent référencer la mémoire tampon constante actuelle au lieu de recréer une.</span><span class="sxs-lookup"><span data-stu-id="db7c8-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="db7c8-128">Il existe deux façons d’obtenir ce résultat souhaité :</span><span class="sxs-lookup"><span data-stu-id="db7c8-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="db7c8-129">Utilisez ID3DX11EffectConstantBuffer :: SetConstantBuffer sur l’effet cloné pour le rendre géré par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="db7c8-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="db7c8-130">Marquer la mémoire tampon de constante en tant que « Single » dans le code HLSL, en forçant le runtime Effect à traiter comme étant géré par l’utilisateur après le clonage</span><span class="sxs-lookup"><span data-stu-id="db7c8-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="db7c8-131">Il existe deux différences entre les deux méthodes ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="db7c8-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="db7c8-132">Tout d’abord, dans la méthode 1, un nouveau ID3D11Buffer sera créé et l’utilisateur avant l’appel de SetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="db7c8-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="db7c8-133">En outre, après avoir appelé UndoSetConstantBuffer dans l’effet cloné, la variable de la méthode 1will pointe vers la mémoire tampon qui vient d’être créée (les effets sont mis à jour lors de l’application), tandis que la variable de la méthode 2 continue à pointer vers la mémoire tampon d’origine (et non à la mettre à jour sur Apply).</span><span class="sxs-lookup"><span data-stu-id="db7c8-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="db7c8-134">Consultez l’exemple suivant en HLSL :</span><span class="sxs-lookup"><span data-stu-id="db7c8-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="db7c8-135">Lors du clonage, l’effet cloné crée un nouveau ID3D11Buffer pour ObjectData et remplit son contenu à la place de l’application, mais référence le ID3D11Buffer d’origine pour ViewData.</span><span class="sxs-lookup"><span data-stu-id="db7c8-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="db7c8-136">Vous pouvez ignorer le qualificateur unique dans le processus de clonage en définissant l' \_ indicateur D3DX11 effet \_ cloner forcer le clone \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="db7c8-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db7c8-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db7c8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db7c8-138">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="db7c8-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




