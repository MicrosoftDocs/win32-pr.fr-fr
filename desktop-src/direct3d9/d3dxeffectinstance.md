---
description: Type de données pour la gestion d’un ensemble de paramètres d’effet par défaut.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: D3DXEFFECTINSTANCE, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322930"
---
# <a name="d3dxeffectinstance-structure"></a><span data-ttu-id="e823b-103">D3DXEFFECTINSTANCE, structure</span><span class="sxs-lookup"><span data-stu-id="e823b-103">D3DXEFFECTINSTANCE structure</span></span>

<span data-ttu-id="e823b-104">Type de données pour la gestion d’un ensemble de paramètres d’effet par défaut.</span><span class="sxs-lookup"><span data-stu-id="e823b-104">Data type for managing a set of default effect parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e823b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e823b-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a><span data-ttu-id="e823b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e823b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e823b-107">**pEffectFilename**</span><span class="sxs-lookup"><span data-stu-id="e823b-107">**pEffectFilename**</span></span>
</dt> <dd>

<span data-ttu-id="e823b-108">Type : **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="e823b-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="e823b-109">Nom du fichier d’effet.</span><span class="sxs-lookup"><span data-stu-id="e823b-109">Name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="e823b-110">**NumDefaults**</span><span class="sxs-lookup"><span data-stu-id="e823b-110">**NumDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="e823b-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e823b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e823b-112">Nombre de paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="e823b-112">Number of default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="e823b-113">**pDefaults**</span><span class="sxs-lookup"><span data-stu-id="e823b-113">**pDefaults**</span></span>
</dt> <dd>

<span data-ttu-id="e823b-114">Type : **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span><span class="sxs-lookup"><span data-stu-id="e823b-114">Type: **[**LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e823b-115">Pointeur vers un tableau d’éléments [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , chacun d’eux contenant un paramètre Effect.</span><span class="sxs-lookup"><span data-stu-id="e823b-115">Pointer to an array of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) elements, each of which contains an effect parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e823b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e823b-116">Requirements</span></span>



| <span data-ttu-id="e823b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e823b-117">Requirement</span></span> | <span data-ttu-id="e823b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e823b-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e823b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e823b-119">Header</span></span><br/> | <dl> <span data-ttu-id="e823b-120"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e823b-120"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e823b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e823b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e823b-122">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="e823b-122">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
