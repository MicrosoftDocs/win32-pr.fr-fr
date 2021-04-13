---
title: fonction glEdgeFlagv (GL. h)
description: Signale les bords comme une limite ou une non-limite. | fonction glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- glEdgeFlagv fonction OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322245"
---
# <a name="gledgeflagv-function"></a><span data-ttu-id="94dd2-105">glEdgeFlagv fonction)</span><span class="sxs-lookup"><span data-stu-id="94dd2-105">glEdgeFlagv function</span></span>

<span data-ttu-id="94dd2-106">Signale les bords comme une limite ou une non-limite.</span><span class="sxs-lookup"><span data-stu-id="94dd2-106">Flags edges as either boundary or nonboundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="94dd2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94dd2-107">Syntax</span></span>


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a><span data-ttu-id="94dd2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94dd2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94dd2-109">*flag*</span><span class="sxs-lookup"><span data-stu-id="94dd2-109">*flag*</span></span> 
</dt> <dd>

<span data-ttu-id="94dd2-110">Spécifie un pointeur vers un tableau qui contient un seul élément booléen, qui remplace la valeur de l’indicateur de bord actuel.</span><span class="sxs-lookup"><span data-stu-id="94dd2-110">Specifies a pointer to an array that contains a single Boolean element, which replaces the current edge flag value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94dd2-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="94dd2-111">Return value</span></span>

<span data-ttu-id="94dd2-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="94dd2-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94dd2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="94dd2-113">Remarks</span></span>

<span data-ttu-id="94dd2-114">Chaque vertex d’un polygone, d’un triangle distinct ou d’un quadrilatère distinct spécifié entre une paire [**glBegin**](/windows/desktop/OpenGL/glbegin) / [**glEnd**](/windows/desktop/OpenGL/glend) est marqué comme le début d’une limite ou d’un bord non limité.</span><span class="sxs-lookup"><span data-stu-id="94dd2-114">Each vertex of a polygon, separate triangle, or separate quadrilateral specified between a [**glBegin**](/windows/desktop/OpenGL/glbegin)/[**glEnd**](/windows/desktop/OpenGL/glend) pair is marked as the start of either a boundary or nonboundary edge.</span></span> <span data-ttu-id="94dd2-115">Si l’indicateur de bord actuel a la **valeur true** lorsque le vertex est spécifié, le vertex est marqué comme le début d’un bord de limite.</span><span class="sxs-lookup"><span data-stu-id="94dd2-115">If the current edge flag is **TRUE** when the vertex is specified, the vertex is marked as the start of a boundary edge.</span></span> <span data-ttu-id="94dd2-116">Si l’indicateur de bord actuel a la **valeur false**, le vertex est marqué comme le début d’un bord non lié.</span><span class="sxs-lookup"><span data-stu-id="94dd2-116">If the current edge flag is **FALSE**, the vertex is marked as the start of a nonboundary edge.</span></span> <span data-ttu-id="94dd2-117">La fonction **glEdgeFlagv** affecte la **valeur true** à l’indicateur Edge si l’indicateur est différent de zéro ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="94dd2-117">The **glEdgeFlagv** function sets the edge flag to **TRUE** if flag is nonzero, **FALSE** otherwise.</span></span>

<span data-ttu-id="94dd2-118">Les vertex des triangles connectés et des quadrilatères connectés sont toujours marqués comme limites, quelle que soit la valeur de l’indicateur de bord.</span><span class="sxs-lookup"><span data-stu-id="94dd2-118">The vertices of connected triangles and connected quadrilaterals are always marked as boundary, regardless of the value of the edge flag.</span></span>

<span data-ttu-id="94dd2-119">Les indicateurs de limite et de périphérie non frontière sur les vertex ne sont significatifs que si le \_ mode de polygone GL \_ est défini sur le point GL ou sur la \_ \_ ligne GL.</span><span class="sxs-lookup"><span data-stu-id="94dd2-119">Boundary and nonboundary edge flags on vertices are significant only if GL\_POLYGON\_MODE is set to GL\_POINT or GL\_LINE.</span></span> <span data-ttu-id="94dd2-120">Consultez [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span><span class="sxs-lookup"><span data-stu-id="94dd2-120">See [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).</span></span>

<span data-ttu-id="94dd2-121">Initialement, le bit de l’indicateur Edge a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="94dd2-121">Initially, the edge flag bit is **TRUE**.</span></span>

<span data-ttu-id="94dd2-122">L’indicateur de périphérie actuel peut être mis à jour à tout moment.</span><span class="sxs-lookup"><span data-stu-id="94dd2-122">The current edge flag can be updated at any time.</span></span> <span data-ttu-id="94dd2-123">En particulier, **glEdgeFlagv** peut être appelé entre un appel à [**glBegin**](/windows/desktop/OpenGL/glbegin) et l’appel correspondant à [**glEnd**](/windows/desktop/OpenGL/glend).</span><span class="sxs-lookup"><span data-stu-id="94dd2-123">In particular, **glEdgeFlagv** can be called between a call to [**glBegin**](/windows/desktop/OpenGL/glbegin) and the corresponding call to [**glEnd**](/windows/desktop/OpenGL/glend).</span></span>

<span data-ttu-id="94dd2-124">Les fonctions suivantes récupèrent les informations relatives à **glEdgeFlagv**:</span><span class="sxs-lookup"><span data-stu-id="94dd2-124">The following functions retrieve information related to **glEdgeFlagv**:</span></span>

<span data-ttu-id="94dd2-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l' \_ indicateur de périphérie de l’argument GL \_</span><span class="sxs-lookup"><span data-stu-id="94dd2-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_EDGE\_FLAG</span></span>

## <a name="requirements"></a><span data-ttu-id="94dd2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94dd2-126">Requirements</span></span>



| <span data-ttu-id="94dd2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94dd2-127">Requirement</span></span> | <span data-ttu-id="94dd2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="94dd2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94dd2-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94dd2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="94dd2-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94dd2-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94dd2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="94dd2-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94dd2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94dd2-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="94dd2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="94dd2-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="94dd2-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="94dd2-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94dd2-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="94dd2-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94dd2-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="94dd2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="94dd2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94dd2-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94dd2-138"><dt>Opengl32.dll</dt></span></span> </dl> |



 

