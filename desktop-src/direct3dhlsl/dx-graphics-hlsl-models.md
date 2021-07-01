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
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119614"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="129d7-103">Modèles de nuanceur et profils Shader</span><span class="sxs-lookup"><span data-stu-id="129d7-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="129d7-104">Le langage d’ombrage de haut niveau pour DirectX implémente une série de modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="129d7-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="129d7-105">En HLSL, vous pouvez créer des nuanceurs programmables de type C pour le pipeline Direct3D.</span><span class="sxs-lookup"><span data-stu-id="129d7-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="129d7-106">Chaque modèle de nuanceur s’appuie sur les fonctionnalités du modèle avant celui-ci, en implémentant davantage de fonctionnalités avec moins de restrictions.</span><span class="sxs-lookup"><span data-stu-id="129d7-106">Each shader model builds on the capabilities of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="129d7-107">Le Shader Model 1 a démarré avec DirectX 8 et inclut des instructions de niveau assembly et de type C.</span><span class="sxs-lookup"><span data-stu-id="129d7-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="129d7-108">Ce modèle présente de nombreuses limitations provoquées par un matériel de nuanceur programmable précoce.</span><span class="sxs-lookup"><span data-stu-id="129d7-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="129d7-109">Les modèles de nuanceur 2 et 3 s’étendent beaucoup sur le nombre d’instructions, et les nuanceurs de constantes pourraient utiliser.</span><span class="sxs-lookup"><span data-stu-id="129d7-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="129d7-110">Elles sont bien plus puissantes que le modèle de nuanceur 1, mais contiennent néanmoins certaines des limitations existantes du premier modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="129d7-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="129d7-111">À compter de Windows Vista, le nuanceur modèle 4 est un remaniement complet.</span><span class="sxs-lookup"><span data-stu-id="129d7-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="129d7-112">Il autorise un nombre illimité d’instructions et de constantes (dans les contraintes matérielles de votre ordinateur), a des objets basés sur des modèles pour rendre le nettoyeur d’échantillonnage de texture et plus efficace, et présente le moins de restrictions de modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="129d7-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="129d7-113">Toutefois, elle nécessite la Windows Driver Model qui est uniquement disponible sur le système d’exploitation Windows Vista (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="129d7-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="129d7-114">Profils de nuanceur</span><span class="sxs-lookup"><span data-stu-id="129d7-114">Shader Profiles</span></span>

<span data-ttu-id="129d7-115">Un profil de nuanceur est la cible de la compilation d’un nuanceur. ce tableau répertorie les profils de nuanceur qui sont pris en charge par chaque modèle de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="129d7-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



| <span data-ttu-id="129d7-116">Modèle de nuanceur</span><span class="sxs-lookup"><span data-stu-id="129d7-116">Shader model</span></span>                                                   | <span data-ttu-id="129d7-117">Profils de nuanceur</span><span class="sxs-lookup"><span data-stu-id="129d7-117">Shader profiles</span></span>                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="129d7-118">Modèle de nuanceur 1</span><span class="sxs-lookup"><span data-stu-id="129d7-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="129d7-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="129d7-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="129d7-120">Nuancier, modèle 2</span><span class="sxs-lookup"><span data-stu-id="129d7-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="129d7-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 0, PS \_ 4 \_ 0 \_ niveau \_ 9 \_ 1, PS \_ 4 0 niveau 9 3, vs 4 0 niveau 9 0, vs 4 0 niveau 9 1, vs 4 0 niveau 9 3 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ , lib \_ 4 \_ 0 \_ niveau \_ 9 \_ 1, lib \_ 4 \_ 0 \_ niveau \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="129d7-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="129d7-122">Modèle de nuanceur 3</span><span class="sxs-lookup"><span data-stu-id="129d7-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="129d7-123">PS \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="129d7-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="129d7-124">Nuanceur modèle 4</span><span class="sxs-lookup"><span data-stu-id="129d7-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="129d7-125">CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="129d7-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="129d7-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="129d7-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="129d7-127">CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (même si GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS 4 \_ \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 et vs \_ 4 \_ 1 ont été introduits dans le modèle de nuanceur 4,0, le modèle de nuanceur 5 ajoute la prise en charge de ces profils de nuanceur pour les</span><span class="sxs-lookup"><span data-stu-id="129d7-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="129d7-128">Shader, modèle 6</span><span class="sxs-lookup"><span data-stu-id="129d7-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="129d7-129">CS \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="129d7-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |

<span data-ttu-id="129d7-130">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="129d7-130">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="129d7-131">Direct3D 9 a introduit les modèles de nuanceur 1, 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="129d7-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span>
- <span data-ttu-id="129d7-132">Direct3D 10 a introduit le nuanceur modèle 4.</span><span class="sxs-lookup"><span data-stu-id="129d7-132">Direct3D 10 introduced shader model 4.</span></span>
- <span data-ttu-id="129d7-133">Direct3D 10,1 a introduit le modèle de nuanceur 4,1.</span><span class="sxs-lookup"><span data-stu-id="129d7-133">Direct3D 10.1 introduced shader model 4.1.</span></span>



 

## <a name="effect-profiles"></a><span data-ttu-id="129d7-134">Profils d’effet</span><span class="sxs-lookup"><span data-stu-id="129d7-134">Effect Profiles</span></span>

<span data-ttu-id="129d7-135">Un profil d’effet est la cible pour la compilation d’un effet/nuanceur ; ce tableau répertorie les profils d’effet pris en charge par chaque version de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="129d7-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>

<span data-ttu-id="129d7-136">Différences entre Direct3D 9 et Direct3D 10 :</span><span class="sxs-lookup"><span data-stu-id="129d7-136">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="129d7-137">Direct3D 9 a introduit Effect-profile des profils FX \_ 1 \_ 0 et FX \_ 2 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="129d7-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span>
- <span data-ttu-id="129d7-138">Direct3D 10 a introduit Effect-Framework Profile FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="129d7-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span>
- <span data-ttu-id="129d7-139">Direct3D 10,1 a introduit Effect-Framework Profile FX \_ 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="129d7-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span>
- <span data-ttu-id="129d7-140">Direct3D 11 a introduit Effect-Framework Profile FX \_ 5 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="129d7-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="129d7-141">Ces profils d’effets hérités sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="129d7-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="129d7-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="129d7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="129d7-143">Référence pour le langage HLSL</span><span class="sxs-lookup"><span data-stu-id="129d7-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





