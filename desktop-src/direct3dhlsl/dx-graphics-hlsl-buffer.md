---
title: Type de mémoire tampon
description: Pour déclarer une variable de mémoire tampon, utilisez la syntaxe ci-après.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Type de mémoire tampon HLSL
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031440"
---
# <a name="buffer-type"></a><span data-ttu-id="e5b1e-104">Type de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="e5b1e-104">Buffer Type</span></span>

<span data-ttu-id="e5b1e-105">Pour déclarer une variable de mémoire tampon, utilisez la syntaxe ci-après.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="e5b1e-106">Buffer< >  *nom* du type ;</span><span class="sxs-lookup"><span data-stu-id="e5b1e-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="e5b1e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5b1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b1e-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Mémoire tampon**</span><span class="sxs-lookup"><span data-stu-id="e5b1e-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="e5b1e-109">Mot clé requis.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="e5b1e-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Entrer*</span><span class="sxs-lookup"><span data-stu-id="e5b1e-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="e5b1e-111">L’un des types HLSL [scalaires](dx-graphics-hlsl-scalar.md), de [vecteur](dx-graphics-hlsl-vector.md)et de [matrice](dx-graphics-hlsl-matrix.md) .</span><span class="sxs-lookup"><span data-stu-id="e5b1e-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="e5b1e-112">Vous pouvez déclarer une variable de mémoire tampon avec une matrice tant qu’elle s’adapte aux quantités de 4 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="e5b1e-113">Vous pouvez donc écrire `Buffer<float2x2>` .</span><span class="sxs-lookup"><span data-stu-id="e5b1e-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="e5b1e-114">Mais `Buffer<float4x4>` est trop grand et le compilateur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="e5b1e-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*</span><span class="sxs-lookup"><span data-stu-id="e5b1e-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="e5b1e-116">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="e5b1e-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="e5b1e-117">Example</span></span>

<span data-ttu-id="e5b1e-118">Voici un exemple de déclaration de mémoire tampon du fichier PipesGS. fx dans l' [exemple PipesGS](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="e5b1e-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="e5b1e-119">Les données sont lues à partir d’une mémoire tampon à l’aide d’une version surchargée de la fonction intrinsèque [**Load**](dx-graphics-hlsl-to-load.md) HLSL qui accepte un paramètre d’entrée (un index d’entiers).</span><span class="sxs-lookup"><span data-stu-id="e5b1e-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="e5b1e-120">Une mémoire tampon est accessible comme un tableau d’éléments ; par conséquent, cet exemple lit le deuxième élément.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="e5b1e-121">Utilisez l' [étape flux-sortie](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) pour sortir des données dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e5b1e-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5b1e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5b1e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b1e-123">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5b1e-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 