---
title: Signatures
description: Une signature de nuanceur est une liste des paramètres qui sont des entrées ou des sorties d’une fonction de nuanceur.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990652"
---
# <a name="signatures"></a><span data-ttu-id="8e66d-103">Signatures</span><span class="sxs-lookup"><span data-stu-id="8e66d-103">Signatures</span></span>

<span data-ttu-id="8e66d-104">Une signature de nuanceur est une liste des paramètres qui sont des entrées ou des sorties d’une fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="8e66d-104">A shader signature is a list of the parameters that are either input to or output from a shader function.</span></span> <span data-ttu-id="8e66d-105">Dans Direct3D 10, les étapes adjacentes partagent efficacement un tableau de registres, où le nuanceur de sortie (ou étape de pipeline) écrit des données à des emplacements spécifiques dans le tableau des registres et le nuanceur d’entrée doit lire les mêmes emplacements.</span><span class="sxs-lookup"><span data-stu-id="8e66d-105">In Direct3D 10, adjacent stages effectively share a register array, where the output shader (or pipeline stage) writes data to specific locations in the register array and the input shader must read from the same locations.</span></span> <span data-ttu-id="8e66d-106">L’API utilise des signatures de nuanceur pour lier les sorties de nuanceur avec des entrées sans la surcharge de la résolution sémantique.</span><span class="sxs-lookup"><span data-stu-id="8e66d-106">The API uses shader signatures to bind shader outputs with inputs without the overhead of semantic resolution.</span></span>

<span data-ttu-id="8e66d-107">Dans Direct3D 10, les signatures d’entrée sont générées à partir d’une déclaration d’entrée de nuanceur et la signature de sortie est générée à partir d’une déclaration de nuanceur-sortie.</span><span class="sxs-lookup"><span data-stu-id="8e66d-107">In Direct3D 10, input signatures are generated from a shader-input declaration and the output signature is generated from a shader-output declaration.</span></span> <span data-ttu-id="8e66d-108">Une signature d’entrée est dite compatible avec une signature de sortie lorsque la signature de sortie est un sous-ensemble strict (type d’argument et correspondance d’ordre) de la signature d’entrée.</span><span class="sxs-lookup"><span data-stu-id="8e66d-108">An input signature is said to be compatible with an output signature when the output signature is a strict subset (argument type and order match) of the input signature.</span></span> <span data-ttu-id="8e66d-109">La méthode la plus simple pour y parvenir consiste à lier les entrées et sorties de nuanceur correspondantes par le même type de structure.</span><span class="sxs-lookup"><span data-stu-id="8e66d-109">The most straightforward way to achieve this is to link corresponding shader inputs and outputs by the same structure type.</span></span>

<span data-ttu-id="8e66d-110">Voici un exemple de signatures compatibles.</span><span class="sxs-lookup"><span data-stu-id="8e66d-110">Here is an example of compatible signatures.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



<span data-ttu-id="8e66d-111">Voici un exemple de signatures incompatibles ; l’ordre des paramètres dans la signature d’entrée ne correspond pas à l’ordre dans la signature de sortie.</span><span class="sxs-lookup"><span data-stu-id="8e66d-111">Here is an example of incompatible signatures; the order of parameters in the input signature does not match the order in the output signature.</span></span>


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



<span data-ttu-id="8e66d-112">PSInWorks est un sous-ensemble compatible de VSOut (les deux premières entrées correspondent à la fois à type et à commande avec les deux premières entrées dans VSOut).</span><span class="sxs-lookup"><span data-stu-id="8e66d-112">PSInWorks is a compatible subset of VSOut (the first two entries match both type and order with the first two entries in VSOut).</span></span> <span data-ttu-id="8e66d-113">Toutefois, PSInFails est incompatible, car le classement ne correspond pas à VSOut.</span><span class="sxs-lookup"><span data-stu-id="8e66d-113">However, PSInFails is incompatible because the ordering does not match with VSOut.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e66d-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e66d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e66d-115">Fonctions</span><span class="sxs-lookup"><span data-stu-id="8e66d-115">Functions</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




