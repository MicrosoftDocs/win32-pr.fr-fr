---
title: fonction glGetClipPlane (GL. h)
description: La fonction glGetClipPlane retourne les coefficients du plan de découpage spécifié.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- glGetClipPlane fonction OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516299"
---
# <a name="glgetclipplane-function"></a><span data-ttu-id="be351-104">glGetClipPlane fonction)</span><span class="sxs-lookup"><span data-stu-id="be351-104">glGetClipPlane function</span></span>

<span data-ttu-id="be351-105">La fonction **glGetClipPlane** retourne les coefficients du plan de découpage spécifié.</span><span class="sxs-lookup"><span data-stu-id="be351-105">The **glGetClipPlane** function returns the coefficients of the specified clipping plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="be351-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be351-106">Syntax</span></span>


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a><span data-ttu-id="be351-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be351-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be351-108">*verticale*</span><span class="sxs-lookup"><span data-stu-id="be351-108">*plane*</span></span> 
</dt> <dd>

<span data-ttu-id="be351-109">Plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="be351-109">A clipping plane.</span></span> <span data-ttu-id="be351-110">Le nombre de plans de découpage dépend de l’implémentation, mais au moins six plans de découpage sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="be351-110">The number of clipping planes depends on the implementation, but at least six clipping planes are supported.</span></span> <span data-ttu-id="be351-111">Ils sont identifiés par des noms symboliques de la forme \_ plan de clip GL \_ *i* où 0 = *i* < des plans de \_ clip GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="be351-111">They are identified by symbolic names of the form GL\_CLIP\_PLANE *i* where 0 = *i* < GL\_MAX\_CLIP\_PLANES.</span></span>

</dd> <dt>

<span data-ttu-id="be351-112">*Sommaire*</span><span class="sxs-lookup"><span data-stu-id="be351-112">*equation*</span></span> 
</dt> <dd>

<span data-ttu-id="be351-113">Retourne quatre valeurs à double précision qui sont les coefficients de l' *équation plane du plan en coordonnées* oculaires.</span><span class="sxs-lookup"><span data-stu-id="be351-113">Returns four double-precision values that are the coefficients of the plane equation of *plane* in eye coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be351-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be351-114">Return value</span></span>

<span data-ttu-id="be351-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be351-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="be351-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="be351-116">Error codes</span></span>

<span data-ttu-id="be351-117">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="be351-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="be351-118">Nom</span><span class="sxs-lookup"><span data-stu-id="be351-118">Name</span></span>                                                                                                  | <span data-ttu-id="be351-119">Signification</span><span class="sxs-lookup"><span data-stu-id="be351-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be351-120"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be351-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="be351-121">le *plan* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="be351-121">*plane* was not an accepted value.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="be351-122"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="be351-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="be351-123">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="be351-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="be351-124">Notes</span><span class="sxs-lookup"><span data-stu-id="be351-124">Remarks</span></span>

<span data-ttu-id="be351-125">La fonction **glGetClipPlane** retourne dans l' *équation* les quatre coefficients de l’équation plane pour le *plan*.</span><span class="sxs-lookup"><span data-stu-id="be351-125">The **glGetClipPlane** function returns in *equation* the four coefficients of the plane equation for *plane*.</span></span>

<span data-ttu-id="be351-126">C’est toujours le cas dans le cadre du \_ plan de clip GL \_ *i* = GL \_ clip \_ PLANE0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="be351-126">It is always the case that GL\_CLIP\_PLANE *i* = GL\_CLIP\_PLANE0 + *i*.</span></span>

<span data-ttu-id="be351-127">Si une erreur est générée, aucune modification n’est apportée au contenu de l' *équation*.</span><span class="sxs-lookup"><span data-stu-id="be351-127">If an error is generated, no change is made to the contents of *equation*.</span></span>

## <a name="requirements"></a><span data-ttu-id="be351-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be351-128">Requirements</span></span>



| <span data-ttu-id="be351-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be351-129">Requirement</span></span> | <span data-ttu-id="be351-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="be351-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be351-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be351-131">Minimum supported client</span></span><br/> | <span data-ttu-id="be351-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be351-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="be351-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be351-133">Minimum supported server</span></span><br/> | <span data-ttu-id="be351-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be351-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be351-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="be351-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="be351-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="be351-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="be351-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be351-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="be351-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be351-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="be351-139">DLL</span><span class="sxs-lookup"><span data-stu-id="be351-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be351-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be351-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be351-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be351-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be351-142">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="be351-142">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="be351-143">**glClipPlane**</span><span class="sxs-lookup"><span data-stu-id="be351-143">**glClipPlane**</span></span>](glclipplane.md)
</dt> <dt>

[<span data-ttu-id="be351-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="be351-144">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





