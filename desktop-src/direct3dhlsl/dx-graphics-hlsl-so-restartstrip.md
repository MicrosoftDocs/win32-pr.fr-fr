---
title: RestartStrip (objet Stream-Output DirectX HLSL)
description: Met fin à la bande primitive en cours et démarre une nouvelle bande. Si la bande actuelle n’a pas assez de vertex émis pour remplir la topologie primitive, la primitive incomplète à la fin sera ignorée.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120194"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a><span data-ttu-id="5d325-104">RestartStrip (objet Stream-Output DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d325-104">RestartStrip (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="5d325-105">Met fin à la bande primitive en cours et démarre une nouvelle bande.</span><span class="sxs-lookup"><span data-stu-id="5d325-105">Ends the current primitive strip and starts a new strip.</span></span> <span data-ttu-id="5d325-106">Si la bande actuelle n’a pas assez de vertex émis pour remplir la topologie primitive, la primitive incomplète à la fin sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="5d325-106">If the current strip does not have enough vertices emitted to fill the primitive topology, the incomplete primitive at the end will be discarded.</span></span>

<span data-ttu-id="5d325-107">RestartStrip();</span><span class="sxs-lookup"><span data-stu-id="5d325-107">RestartStrip();</span></span>



 

## <a name="parameters"></a><span data-ttu-id="5d325-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d325-108">Parameters</span></span>



| <span data-ttu-id="5d325-109">Élément</span><span class="sxs-lookup"><span data-stu-id="5d325-109">Item</span></span>                                                                                     | <span data-ttu-id="5d325-110">Description</span><span class="sxs-lookup"><span data-stu-id="5d325-110">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="5d325-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span><span class="sxs-lookup"><span data-stu-id="5d325-111"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None**</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="5d325-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5d325-112">Return Value</span></span>

<span data-ttu-id="5d325-113">None</span><span class="sxs-lookup"><span data-stu-id="5d325-113">None</span></span>

## <a name="remarks"></a><span data-ttu-id="5d325-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d325-114">Remarks</span></span>

<span data-ttu-id="5d325-115">Une bande coupée provoque la fin de la bande actuelle et une nouvelle bande.</span><span class="sxs-lookup"><span data-stu-id="5d325-115">A strip cut causes the current strip to end, and a new strip to start.</span></span> <span data-ttu-id="5d325-116">Une bande peut être effectuée en appelant explicitement cette méthode, ou simplement en affichant jusqu’à la valeur d’index maximale (1, qui est 0xFFFFFFFF pour les index 32 bits ou 0xFFFF pour les index 16 bits).</span><span class="sxs-lookup"><span data-stu-id="5d325-116">A strip cut can be done by explicitly calling this method, or just by rendering up to the maximum index value ( 1, which is 0xffffffff for 32-bit indices or 0xffff for 16-bit indices).</span></span> <span data-ttu-id="5d325-117">Chaque instance d’un dessin indexé avec une instance indexée génère automatiquement une bande.</span><span class="sxs-lookup"><span data-stu-id="5d325-117">Each instance of an indexed-instanced draw generates a strip cut automatically.</span></span> <span data-ttu-id="5d325-118">Cela est vrai même si la topologie n’est pas une bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="5d325-118">This is true even if the topology is not a triangle strip.</span></span>

> [!Note]  
> <span data-ttu-id="5d325-119">La prise en charge du redémarrage et de la « valeur magique » pour une coupe est uniquement disponible sur les appareils de [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 ou ultérieur.</span><span class="sxs-lookup"><span data-stu-id="5d325-119">Support for restart and the  1 'magic value' for a cut is only available on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 or higher devices.</span></span>

 

<span data-ttu-id="5d325-120">La sortie est toujours supposée être une bande triangulaire.</span><span class="sxs-lookup"><span data-stu-id="5d325-120">The output is always assumed to be a triangle strip.</span></span> <span data-ttu-id="5d325-121">Pour transformer la sortie en une liste de triangles, vous devez appeler RestartStrip entre chaque triangle.</span><span class="sxs-lookup"><span data-stu-id="5d325-121">To make the output a triangle list, you must call RestartStrip between each triangle.</span></span> <span data-ttu-id="5d325-122">Les ventilateurs triangulaires ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5d325-122">Triangle fans are unsupported.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="5d325-123">Modèle de nuanceur minimal</span><span class="sxs-lookup"><span data-stu-id="5d325-123">Minimum Shader Model</span></span>

<span data-ttu-id="5d325-124">Cette fonction est prise en charge dans les modèles de nuanceur suivants.</span><span class="sxs-lookup"><span data-stu-id="5d325-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5d325-125">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="5d325-125">Shader Model</span></span>                                              | <span data-ttu-id="5d325-126">Prise en charge</span><span class="sxs-lookup"><span data-stu-id="5d325-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5d325-127">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="5d325-127">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5d325-128">yes</span><span class="sxs-lookup"><span data-stu-id="5d325-128">yes</span></span>       |
| [<span data-ttu-id="5d325-129">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d325-129">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5d325-130">Non</span><span class="sxs-lookup"><span data-stu-id="5d325-130">no</span></span>        |
| [<span data-ttu-id="5d325-131">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d325-131">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5d325-132">Non</span><span class="sxs-lookup"><span data-stu-id="5d325-132">no</span></span>        |
| [<span data-ttu-id="5d325-133">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5d325-133">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5d325-134">Non</span><span class="sxs-lookup"><span data-stu-id="5d325-134">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5d325-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5d325-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d325-136">Stream-sortie (objet)</span><span class="sxs-lookup"><span data-stu-id="5d325-136">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

