---
title: fonction glLoadIdentity (GL. h)
description: La fonction glLoadIdentity remplace la matrice actuelle par la matrice d’identité.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- glLoadIdentity fonction OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104559053"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="a70ea-104">glLoadIdentity fonction)</span><span class="sxs-lookup"><span data-stu-id="a70ea-104">glLoadIdentity function</span></span>

<span data-ttu-id="a70ea-105">La fonction **glLoadIdentity** remplace la matrice actuelle par la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="a70ea-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a70ea-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a70ea-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="a70ea-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a70ea-107">Parameters</span></span>

<span data-ttu-id="a70ea-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a70ea-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a70ea-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a70ea-109">Return value</span></span>

<span data-ttu-id="a70ea-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a70ea-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a70ea-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a70ea-111">Error codes</span></span>

<span data-ttu-id="a70ea-112">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a70ea-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a70ea-113">Nom</span><span class="sxs-lookup"><span data-stu-id="a70ea-113">Name</span></span>                                                                                                  | <span data-ttu-id="a70ea-114">Signification</span><span class="sxs-lookup"><span data-stu-id="a70ea-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a70ea-115"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a70ea-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a70ea-116">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a70ea-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a70ea-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a70ea-117">Remarks</span></span>

<span data-ttu-id="a70ea-118">La fonction **glLoadIdentity** remplace la matrice actuelle par la matrice d’identité.</span><span class="sxs-lookup"><span data-stu-id="a70ea-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="a70ea-119">Il est sémantiquement équivalent à l’appel de [**glLoadMatrix**](glloadmatrix.md) avec la matrice d’identité suivante.</span><span class="sxs-lookup"><span data-stu-id="a70ea-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![Diagramme montrant la matrice d’identité appelée par glLoadIdentity.](images/load01.png)

<span data-ttu-id="a70ea-121">Toutefois, dans certains cas, il est plus efficace.</span><span class="sxs-lookup"><span data-stu-id="a70ea-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="a70ea-122">Les fonctions suivantes récupèrent les informations relatives à **glLoadIdentity**:</span><span class="sxs-lookup"><span data-stu-id="a70ea-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="a70ea-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="a70ea-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="a70ea-124">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="a70ea-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="a70ea-125">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="a70ea-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="a70ea-126">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="a70ea-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="a70ea-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a70ea-127">Requirements</span></span>



| <span data-ttu-id="a70ea-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a70ea-128">Requirement</span></span> | <span data-ttu-id="a70ea-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="a70ea-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a70ea-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a70ea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a70ea-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a70ea-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a70ea-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a70ea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a70ea-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a70ea-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a70ea-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a70ea-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a70ea-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a70ea-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a70ea-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a70ea-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="a70ea-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a70ea-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a70ea-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a70ea-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a70ea-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a70ea-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a70ea-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a70ea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70ea-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a70ea-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a70ea-142">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="a70ea-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a70ea-143">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="a70ea-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="a70ea-144">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="a70ea-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="a70ea-145">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="a70ea-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="a70ea-146">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="a70ea-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





