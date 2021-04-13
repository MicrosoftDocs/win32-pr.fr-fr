---
description: Cette macro crée une valeur utilisée par le problème pour émettre une fin de requête.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323010"
---
# <a name="d3dissue_end"></a><span data-ttu-id="27088-103">Fin de D3DISSUE \_</span><span class="sxs-lookup"><span data-stu-id="27088-103">D3DISSUE\_END</span></span>

<span data-ttu-id="27088-104">Cette macro crée une valeur utilisée par le [**problème**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) pour émettre une fin de requête.</span><span class="sxs-lookup"><span data-stu-id="27088-104">This macro creates a value used by [**Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) to issue a query end.</span></span>

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a><span data-ttu-id="27088-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27088-105">Parameters</span></span>





 

## <a name="remarks"></a><span data-ttu-id="27088-106">Notes</span><span class="sxs-lookup"><span data-stu-id="27088-106">Remarks</span></span>

<span data-ttu-id="27088-107">Cette macro remplace l’état de la requête par non signalé.</span><span class="sxs-lookup"><span data-stu-id="27088-107">This macro changes the query state to nonsignaled.</span></span>

<span data-ttu-id="27088-108">D3DISSUE \_ end est valide pour les types de requêtes suivants.</span><span class="sxs-lookup"><span data-stu-id="27088-108">D3DISSUE\_END is valid for the following query types.</span></span>

-   <span data-ttu-id="27088-109">D3DQUERYTYPE \_ Vcache</span><span class="sxs-lookup"><span data-stu-id="27088-109">D3DQUERYTYPE\_VCACHE</span></span>
-   <span data-ttu-id="27088-110">D3DQUERYTYPE \_ ResourceManager</span><span class="sxs-lookup"><span data-stu-id="27088-110">D3DQUERYTYPE\_ResourceManager</span></span>
-   <span data-ttu-id="27088-111">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="27088-111">D3DQUERYTYPE\_VERTEXSTATS</span></span>
-   <span data-ttu-id="27088-112">\_Événement D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="27088-112">D3DQUERYTYPE\_EVENT</span></span>
-   <span data-ttu-id="27088-113">\_Occlusion D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="27088-113">D3DQUERYTYPE\_OCCLUSION</span></span>

## <a name="requirements"></a><span data-ttu-id="27088-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27088-114">Requirements</span></span>



| <span data-ttu-id="27088-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27088-115">Requirement</span></span> | <span data-ttu-id="27088-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="27088-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27088-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="27088-117">Header</span></span><br/> | <dl> <span data-ttu-id="27088-118"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="27088-118"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27088-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27088-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27088-120">Macros</span><span class="sxs-lookup"><span data-stu-id="27088-120">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="27088-121">**Début de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="27088-121">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md)
</dt> <dt>

[<span data-ttu-id="27088-122">**D3DQUERYTYPE**</span><span class="sxs-lookup"><span data-stu-id="27088-122">**D3DQUERYTYPE**</span></span>](./d3dquerytype.md)
</dt> </dl>

 

 
