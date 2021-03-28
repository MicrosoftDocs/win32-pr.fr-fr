---
title: Référence pour le langage HLSL
description: La documentation de référence HLSL spécifie les caractéristiques du langage. Il est divisé en plusieurs sections.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029597"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="a0d21-104">Référence pour le langage HLSL</span><span class="sxs-lookup"><span data-stu-id="a0d21-104">Reference for HLSL</span></span>

<span data-ttu-id="a0d21-105">La documentation de référence HLSL spécifie les caractéristiques du langage.</span><span class="sxs-lookup"><span data-stu-id="a0d21-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="a0d21-106">Il est divisé en plusieurs sections.</span><span class="sxs-lookup"><span data-stu-id="a0d21-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="a0d21-107">[Syntaxe du langage (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) -les nuanceurs de programmation en HLSL requièrent que vous compreniez la syntaxe du langage, autrement dit, la façon dont vous écrivez le code HLSL.</span><span class="sxs-lookup"><span data-stu-id="a0d21-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="a0d21-108">Cela comprend le code permettant de déclarer et d’initialiser des variables, d’écrire des fonctions de nuanceur définies par l’utilisateur et d’ajouter des instructions de contrôle de Flow pour rendre vos fonctions plus puissantes.</span><span class="sxs-lookup"><span data-stu-id="a0d21-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="a0d21-109">[Modèles de nuanceur et profils de nuanceur](dx-graphics-hlsl-models.md) -le compilateur HLSL implémente des règles et des restrictions basées sur les modèles de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a0d21-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="a0d21-110">Le code de chaque nuanceur de sommets, nuanceur de géométrie (si vous utilisez Direct3D 10) et le nuanceur de pixels sont validés par rapport à un modèle de nuanceur, que vous fournissez au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="a0d21-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="a0d21-111">[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL possède de nombreuses fonctions intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="a0d21-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="a0d21-112">Celles-ci sont implémentées et testées afin que vous puissiez les utiliser, sachant qu’elles sont déjà déboguées et qu’elles fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="a0d21-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="a0d21-113">Si vous choisissez d’écrire vos propres fonctions, consultez la section syntaxe de langage pour l’écriture de fonctions définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0d21-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="a0d21-114">[Référence du nuanceur asm](dx9-graphics-reference-asm.md) : instructions d’assembly que vous pouvez utiliser pour programmer et déboguer des nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="a0d21-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="a0d21-115">[Référence D3DCompiler](dx-graphics-d3dcompiler-reference.md) : compile la source HLSL brute.</span><span class="sxs-lookup"><span data-stu-id="a0d21-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="a0d21-116">[Référence de conversion de format Inline](inline-format-conversion-reference.md) : le \_ fichier D3DX DXGIFormatConvert. inl contient des fonctions de conversion de format Inline que vous pouvez utiliser dans le nuanceur de calcul ou le nuanceur de pixels sur du matériel Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="a0d21-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="a0d21-117">Vous pouvez utiliser ces fonctions dans votre application pour lire et écrire simultanément dans une texture.</span><span class="sxs-lookup"><span data-stu-id="a0d21-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="a0d21-118">Autrement dit, vous pouvez effectuer une modification d’image sur place.</span><span class="sxs-lookup"><span data-stu-id="a0d21-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="a0d21-119">Pour utiliser ces fonctions de conversion de format Inline, incluez le \_ fichier D3DX DXGIFormatConvert. inl dans votre application.</span><span class="sxs-lookup"><span data-stu-id="a0d21-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="a0d21-120">[Annexe (DirectX HLSL)](dx-graphics-hlsl-appendix.md) -l’annexe est incluse à des fins d’exhaustivité.</span><span class="sxs-lookup"><span data-stu-id="a0d21-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="a0d21-121">Il comprend une liste des mots clés et des mots réservés. ces mots ne peuvent pas être utilisés comme identificateurs dans vos programmes.</span><span class="sxs-lookup"><span data-stu-id="a0d21-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="a0d21-122">Il comprend également une liste de la grammaire de la langue à des fins de référence.</span><span class="sxs-lookup"><span data-stu-id="a0d21-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="a0d21-123">[**Erreurs et avertissements HLSL**](hlsl-errors-and-warnings.md) -fournit des codes d’erreur et d’avertissement qu’un nuanceur peut retourner.</span><span class="sxs-lookup"><span data-stu-id="a0d21-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0d21-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0d21-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0d21-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="a0d21-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="a0d21-126">Guide de programmation pour HLSL</span><span class="sxs-lookup"><span data-stu-id="a0d21-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




