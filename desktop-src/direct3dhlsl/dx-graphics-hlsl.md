---
title: HLSL (High-Level Shader Language)
description: Le langage HLSL est le langage de nuanceur de haut niveau de type C que vous utilisez avec les nuanceurs programmables dans DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104973894"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="ee615-103">HLSL (High-Level Shader Language)</span><span class="sxs-lookup"><span data-stu-id="ee615-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="ee615-104">Le langage HLSL est le langage de nuanceur de haut niveau de type C que vous utilisez avec les nuanceurs programmables dans DirectX.</span><span class="sxs-lookup"><span data-stu-id="ee615-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="ee615-105">Par exemple, vous pouvez utiliser le langage HLSL pour écrire un [nuanceur de sommets](../direct3d11/vertex-shader-stage.md)ou un [nuanceur de pixels](../direct3d11/pixel-shader-stage.md), et utiliser ces nuanceurs dans l’implémentation du convertisseur dans votre application [Direct3D](../direct3d12/directx-12-programming-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="ee615-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="ee615-106">Vous pouvez aussi utiliser le langage HLSL pour écrire un nuanceur de calcul, par exemple pour implémenter une simulation physique.</span><span class="sxs-lookup"><span data-stu-id="ee615-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="ee615-107">Toutefois, si, par exemple, vous allez écrire votre propre opérateur de convolution (pour le traitement d’image) en langage HLSL dans un nuanceur de calcul, vous obtiendrez de meilleures performances dans ce scénario si vous utilisez [Direct machine learning (DirectML)](../direct3d12/dml.md) .</span><span class="sxs-lookup"><span data-stu-id="ee615-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="ee615-108">Le langage HLSL a été créé (à partir de DirectX 9) pour configurer le [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programmable.</span><span class="sxs-lookup"><span data-stu-id="ee615-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="ee615-109">Vous pouvez programmer l’intégralité du pipeline avec des instructions HLSL.</span><span class="sxs-lookup"><span data-stu-id="ee615-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="ee615-110">Emplacement suivant</span><span class="sxs-lookup"><span data-stu-id="ee615-110">Where to go next</span></span>

* [<span data-ttu-id="ee615-111">Guide de programmation pour le HLSL</span><span class="sxs-lookup"><span data-stu-id="ee615-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="ee615-112">Référence pour le langage HLSL</span><span class="sxs-lookup"><span data-stu-id="ee615-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="ee615-113">Guide de programmation pour le HLSL</span><span class="sxs-lookup"><span data-stu-id="ee615-113">Programming guide for HLSL</span></span>

<span data-ttu-id="ee615-114">Pour une présentation conceptuelle du langage HLSL, consultez le [Guide de programmation pour le langage HLSL](./dx-graphics-hlsl-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="ee615-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="ee615-115">Le Guide de programmation aborde les différents types de phases de nuanceur et explique comment créer, compiler, optimiser, lier et lier des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="ee615-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="ee615-116">Vous y trouverez également des présentations et des notes de publication sur, les générations successives de la version du modèle de nuanceur qui ont été publiées, en remontant en ce qui concerne le nuancier HLSL Model 5.</span><span class="sxs-lookup"><span data-stu-id="ee615-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="ee615-117">Référence pour le langage HLSL</span><span class="sxs-lookup"><span data-stu-id="ee615-117">Reference for HLSL</span></span>

<span data-ttu-id="ee615-118">Pour obtenir de la documentation de référence sur HLSL, consultez la [référence pour HLSL](./dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ee615-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="ee615-119">La section de référence contient une liste complète de la syntaxe du langage et des fonctions intrinsèques qui sont intégrées en HLSL afin de simplifier vos exigences de codage.</span><span class="sxs-lookup"><span data-stu-id="ee615-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="ee615-120">Vous y trouverez également une discussion sur les modèles de nuanceur et les profils, et le contenu de référence du modèle de nuanceur en retour en tant que nuanceur HLSL modèle 1.</span><span class="sxs-lookup"><span data-stu-id="ee615-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="ee615-121">Il y a également du contenu qui couvre des instructions d’assembly, l’outil D3DCompiler et des informations sur les erreurs et avertissements qu’un nuanceur peut retourner.</span><span class="sxs-lookup"><span data-stu-id="ee615-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>