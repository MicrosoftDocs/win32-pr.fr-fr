---
title: Type de vecteur (HLSL)
description: Un vecteur contient entre un et quatre composants scalaires ; chaque composant d’un vecteur doit être du même type.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Type de vecteur HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104991853"
---
# <a name="vector-type"></a><span data-ttu-id="12be7-104">Type de vecteur</span><span class="sxs-lookup"><span data-stu-id="12be7-104">Vector Type</span></span>

<span data-ttu-id="12be7-105">Un vecteur contient entre un et quatre composants scalaires ; chaque composant d’un vecteur doit être du même type.</span><span class="sxs-lookup"><span data-stu-id="12be7-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="12be7-106">**Nom de TypeNumber**</span><span class="sxs-lookup"><span data-stu-id="12be7-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="12be7-107">Components</span><span class="sxs-lookup"><span data-stu-id="12be7-107">Components</span></span>



| <span data-ttu-id="12be7-108">Élément</span><span class="sxs-lookup"><span data-stu-id="12be7-108">Item</span></span>                                                                                                                             | <span data-ttu-id="12be7-109">Description</span><span class="sxs-lookup"><span data-stu-id="12be7-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12be7-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="12be7-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="12be7-111">Nom unique qui contient deux parties.</span><span class="sxs-lookup"><span data-stu-id="12be7-111">A single name that contains two parts.</span></span> <span data-ttu-id="12be7-112">La première partie est l’un des types [scalaires](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="12be7-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="12be7-113">La deuxième partie est le nombre de composants, qui doit être compris entre 1 et 4 inclus.</span><span class="sxs-lookup"><span data-stu-id="12be7-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="12be7-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**</span><span class="sxs-lookup"><span data-stu-id="12be7-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="12be7-115">Chaîne ASCII qui identifie de façon unique le nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="12be7-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="12be7-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="12be7-116">Examples</span></span>

<span data-ttu-id="12be7-117">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="12be7-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="12be7-118">Un vecteur peut être déclaré à l’aide de cette syntaxe également :</span><span class="sxs-lookup"><span data-stu-id="12be7-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="12be7-119">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="12be7-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="12be7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12be7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12be7-121">Types de données (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12be7-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





