---
title: Modèles de nuanceur et profils Shader
description: Modèles de nuanceur et profils Shader
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840561"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="054c2-103">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="054c2-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="054c2-104">Le langage d’ombrage de haut niveau pour DirectX implémente une série de modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="054c2-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="054c2-105">En HLSL, vous pouvez créer des nuanceurs programmables de type C pour le pipeline Direct3D.</span><span class="sxs-lookup"><span data-stu-id="054c2-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="054c2-106">Chaque modèle de nuanceur s’appuie sur les capacités du modèle avant celui-ci, en implémentant davantage de fonctionnalités avec moins de restrictions.</span><span class="sxs-lookup"><span data-stu-id="054c2-106">Each shader model builds on the capabilites of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="054c2-107">Le Shader Model 1 a démarré avec DirectX 8 et inclut des instructions de niveau assembly et de type C.</span><span class="sxs-lookup"><span data-stu-id="054c2-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="054c2-108">Ce modèle présente de nombreuses limitations provoquées par un matériel de nuanceur programmable précoce.</span><span class="sxs-lookup"><span data-stu-id="054c2-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="054c2-109">Les modèles de nuanceur 2 et 3 s’étendent beaucoup sur le nombre d’instructions, et les nuanceurs de constantes pourraient utiliser.</span><span class="sxs-lookup"><span data-stu-id="054c2-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="054c2-110">Elles sont bien plus puissantes que le modèle de nuanceur 1, mais contiennent néanmoins certaines des limitations existantes du premier modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="054c2-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="054c2-111">À compter de Windows Vista, le nuanceur modèle 4 est un remaniement complet.</span><span class="sxs-lookup"><span data-stu-id="054c2-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="054c2-112">Il autorise un nombre illimité d’instructions et de constantes (dans les contraintes matérielles de votre ordinateur), a des objets basés sur des modèles pour rendre le nettoyeur d’échantillonnage de texture et plus efficace, et présente le moins de restrictions de modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="054c2-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="054c2-113">Toutefois, elle nécessite la Windows Driver Model qui est uniquement disponible sur le système d’exploitation Windows Vista (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="054c2-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="054c2-114">Profils de nuanceur</span><span class="sxs-lookup"><span data-stu-id="054c2-114">Shader Profiles</span></span>

<span data-ttu-id="054c2-115">Un profil de nuanceur est la cible de la compilation d’un nuanceur. ce tableau répertorie les profils de nuanceur qui sont pris en charge par chaque modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="054c2-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054c2-116">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="054c2-116">Shader Model</span></span>                                       | <span data-ttu-id="054c2-117">Profils de nuanceur</span><span class="sxs-lookup"><span data-stu-id="054c2-117">Shader Profiles</span></span>                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="054c2-118">Modèle de nuanceur 1</span><span class="sxs-lookup"><span data-stu-id="054c2-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="054c2-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="054c2-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="054c2-120">Nuancier, modèle 2</span><span class="sxs-lookup"><span data-stu-id="054c2-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="054c2-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 0, PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1, PS \_ 4 0 niveau 9 3, vs 4 0 niveau 9 0, vs 4 0 niveau 9 1, vs 4 0 niveau 9 3 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , lib \_ 4 \_ 0 \_ niveau \_ 9 \_ 1, lib \_ 4 \_ 0 \_ niveau \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="054c2-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="054c2-122">Modèle de nuanceur 3</span><span class="sxs-lookup"><span data-stu-id="054c2-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="054c2-123">PS \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="054c2-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="054c2-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="054c2-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="054c2-125">CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="054c2-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="054c2-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="054c2-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="054c2-127">CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (même si GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS 4 \_ \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 et vs \_ 4 \_ 1 ont été introduits dans le modèle de nuanceur 4,0, le modèle de nuanceur 5 ajoute la prise en charge de ces profils de nuanceur pour les</span><span class="sxs-lookup"><span data-stu-id="054c2-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="054c2-128">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="054c2-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="054c2-129">CS \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="054c2-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054c2-130">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="054c2-130">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="054c2-131">Direct3D 9 a introduit les modèles de nuanceur 1, 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="054c2-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span><br/> <span data-ttu-id="054c2-132">Direct3D 10 a introduit le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="054c2-132">Direct3D 10 introduced shader model 4.</span></span><br/> <span data-ttu-id="054c2-133">Direct3D 10,1 a introduit le modèle de nuanceur 4,1.</span><span class="sxs-lookup"><span data-stu-id="054c2-133">Direct3D 10.1 introduced shader model 4.1.</span></span><br/> |



 

## <a name="effect-profiles"></a><span data-ttu-id="054c2-134">Profils d’effet</span><span class="sxs-lookup"><span data-stu-id="054c2-134">Effect Profiles</span></span>

<span data-ttu-id="054c2-135">Un profil d’effet est la cible pour la compilation d’un effet/nuanceur ; ce tableau répertorie les profils d’effet pris en charge par chaque version de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="054c2-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="054c2-136">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="054c2-136">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="054c2-137">Direct3D 9 a introduit Effect-profile des profils FX \_ 1 \_ 0 et FX \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="054c2-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span><br/> <span data-ttu-id="054c2-138">Direct3D 10 a introduit Effect-Framework Profile FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="054c2-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span><br/> <span data-ttu-id="054c2-139">Direct3D 10,1 a introduit Effect-Framework Profile FX \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="054c2-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span><br/> <span data-ttu-id="054c2-140">Direct3D 11 a introduit Effect-Framework Profile FX \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="054c2-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="054c2-141">Ces profils d’effets hérités sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="054c2-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="054c2-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="054c2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="054c2-143">Référence pour le langage HLSL</span><span class="sxs-lookup"><span data-stu-id="054c2-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





