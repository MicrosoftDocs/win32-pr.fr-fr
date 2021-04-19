---
description: Créez un jeton de numéro de version de nuanceur de vertex.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: Macro D3DVS_VERSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537264"
---
# <a name="d3dvs_version-macro"></a><span data-ttu-id="e42ff-103">D3DVS la \_ macro de version</span><span class="sxs-lookup"><span data-stu-id="e42ff-103">D3DVS\_VERSION macro</span></span>

<span data-ttu-id="e42ff-104">Créez un jeton de numéro de version de nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="e42ff-104">Create a vertex shader version number token.</span></span>

## <a name="syntax"></a><span data-ttu-id="e42ff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e42ff-105">Syntax</span></span>


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a><span data-ttu-id="e42ff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e42ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42ff-107">*\_Majeure*</span><span class="sxs-lookup"><span data-stu-id="e42ff-107">*\_Major*</span></span> 
</dt> <dd>

<span data-ttu-id="e42ff-108">Version principale du nuanceur de vertex.</span><span class="sxs-lookup"><span data-stu-id="e42ff-108">The major vertex shader version.</span></span> <span data-ttu-id="e42ff-109">Consultez la section Notes pour connaître les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="e42ff-109">See remarks for appropriate values.</span></span>

</dd> <dt>

<span data-ttu-id="e42ff-110">*\_Secondaire*</span><span class="sxs-lookup"><span data-stu-id="e42ff-110">*\_Minor*</span></span> 
</dt> <dd>

<span data-ttu-id="e42ff-111">Version mineure du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="e42ff-111">The minor vertex shader version.</span></span> <span data-ttu-id="e42ff-112">Consultez la section Notes pour connaître les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="e42ff-112">See remarks for appropriate values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42ff-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e42ff-113">Return value</span></span>

<span data-ttu-id="e42ff-114">Retourne une valeur DWORD qui est une version du nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="e42ff-114">Returns a DWORD value that is a vertex shader version.</span></span>

## <a name="remarks"></a><span data-ttu-id="e42ff-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e42ff-115">Remarks</span></span>

<span data-ttu-id="e42ff-116">Numéros de versions</span><span class="sxs-lookup"><span data-stu-id="e42ff-116">Version Numbers</span></span>

<span data-ttu-id="e42ff-117">Le numéro de version est une combinaison de la version principale et des numéros de version de nuanceur de vertex secondaires.</span><span class="sxs-lookup"><span data-stu-id="e42ff-117">The version number is a combination of the major version and the minor vertex shader version numbers.</span></span> <span data-ttu-id="e42ff-118">Les nombres valides sont indiqués dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="e42ff-118">Valid numbers are shown in the table.</span></span>



| <span data-ttu-id="e42ff-119">Majeure</span><span class="sxs-lookup"><span data-stu-id="e42ff-119">Major</span></span> | <span data-ttu-id="e42ff-120">Secondaire</span><span class="sxs-lookup"><span data-stu-id="e42ff-120">Minor</span></span> | <span data-ttu-id="e42ff-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="e42ff-121">Example</span></span>             |
|-------|-------|---------------------|
| <span data-ttu-id="e42ff-122">1</span><span class="sxs-lookup"><span data-stu-id="e42ff-122">1</span></span>     | <span data-ttu-id="e42ff-123">1</span><span class="sxs-lookup"><span data-stu-id="e42ff-123">1</span></span>     | <span data-ttu-id="e42ff-124">\_Version de D3DVS (1, 1)</span><span class="sxs-lookup"><span data-stu-id="e42ff-124">D3DVS\_VERSION(1,1)</span></span> |
| <span data-ttu-id="e42ff-125">2</span><span class="sxs-lookup"><span data-stu-id="e42ff-125">2</span></span>     | <span data-ttu-id="e42ff-126">0</span><span class="sxs-lookup"><span data-stu-id="e42ff-126">0</span></span>     | <span data-ttu-id="e42ff-127">\_Version de D3DVS (2, 0)</span><span class="sxs-lookup"><span data-stu-id="e42ff-127">D3DVS\_VERSION(2,0)</span></span> |
| <span data-ttu-id="e42ff-128">3</span><span class="sxs-lookup"><span data-stu-id="e42ff-128">3</span></span>     | <span data-ttu-id="e42ff-129">0</span><span class="sxs-lookup"><span data-stu-id="e42ff-129">0</span></span>     | <span data-ttu-id="e42ff-130">\_Version de D3DVS (3, 0)</span><span class="sxs-lookup"><span data-stu-id="e42ff-130">D3DVS\_VERSION(3,0)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="e42ff-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e42ff-131">Requirements</span></span>



| <span data-ttu-id="e42ff-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e42ff-132">Requirement</span></span> | <span data-ttu-id="e42ff-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e42ff-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e42ff-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e42ff-134">Header</span></span><br/> | <dl> <span data-ttu-id="e42ff-135"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e42ff-135"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e42ff-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e42ff-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42ff-137">Macros</span><span class="sxs-lookup"><span data-stu-id="e42ff-137">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




