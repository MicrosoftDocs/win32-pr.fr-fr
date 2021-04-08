---
title: gluErrorString, fonction (Glu. h)
description: La fonction gluErrorString génère une chaîne d’erreur à partir d’un code d’erreur OpenGL ou GLU. La chaîne d’erreur est ANSI uniquement.
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString fonction OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741117"
---
# <a name="gluerrorstring-function"></a><span data-ttu-id="af5f1-105">gluErrorString fonction)</span><span class="sxs-lookup"><span data-stu-id="af5f1-105">gluErrorString function</span></span>

<span data-ttu-id="af5f1-106">La fonction **gluErrorString** génère une chaîne d’erreur à partir d’un code d’erreur OpenGL ou Glu.</span><span class="sxs-lookup"><span data-stu-id="af5f1-106">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="af5f1-107">La chaîne d’erreur est ANSI uniquement.</span><span class="sxs-lookup"><span data-stu-id="af5f1-107">The error string is ANSI only.</span></span>

## <a name="syntax"></a><span data-ttu-id="af5f1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af5f1-108">Syntax</span></span>


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a><span data-ttu-id="af5f1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af5f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af5f1-110">*errCode*</span><span class="sxs-lookup"><span data-stu-id="af5f1-110">*errCode*</span></span> 
</dt> <dd>

<span data-ttu-id="af5f1-111">Code d’erreur OpenGL ou GLU.</span><span class="sxs-lookup"><span data-stu-id="af5f1-111">An OpenGL or GLU error code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af5f1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="af5f1-112">Remarks</span></span>

<span data-ttu-id="af5f1-113">La fonction **gluErrorString** génère une chaîne d’erreur à partir d’un code d’erreur OpenGL ou Glu.</span><span class="sxs-lookup"><span data-stu-id="af5f1-113">The **gluErrorString** function produces an error string from an OpenGL or GLU error code.</span></span> <span data-ttu-id="af5f1-114">La chaîne est au format ISO Latin 1.</span><span class="sxs-lookup"><span data-stu-id="af5f1-114">The string is in an ISO Latin 1 format.</span></span> <span data-ttu-id="af5f1-115">Par exemple, **gluErrorString**(GL \_ de mémoire insuffisante \_ \_ ) retourne la chaîne « mémoire insuffisante ».</span><span class="sxs-lookup"><span data-stu-id="af5f1-115">For example, **gluErrorString**(GL\_OUT\_OF\_MEMORY) returns the string "out of memory".</span></span>

<span data-ttu-id="af5f1-116">Les codes d’erreur GLU standard sont \_ Glu \_ enum non valide, Glu \_ valeur non valide \_ et Glu \_ mémoire insuffisante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="af5f1-116">The standard GLU error codes are GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY.</span></span> <span data-ttu-id="af5f1-117">Certaines autres fonctions GLU peuvent retourner des codes d’erreur spécialisés par le biais de rappels.</span><span class="sxs-lookup"><span data-stu-id="af5f1-117">Certain other GLU functions can return specialized error codes through callbacks.</span></span> <span data-ttu-id="af5f1-118">Pour obtenir la liste des codes d’erreur OpenGL, consultez [**glGetError**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="af5f1-118">For the list of OpenGL error codes, see [**glGetError**](glgeterror.md).</span></span>

<span data-ttu-id="af5f1-119">La fonction **gluErrorString** génère des chaînes d’erreur en ANSI uniquement.</span><span class="sxs-lookup"><span data-stu-id="af5f1-119">The **gluErrorString** function produces error strings in ANSI only.</span></span> <span data-ttu-id="af5f1-120">Dans la mesure du possible, utilisez **gluErrorStringWIN**, qui autorise les chaînes d’erreur ANSI ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="af5f1-120">Whenever possible, use **gluErrorStringWIN**, which allows ANSI or Unicode error strings.</span></span> <span data-ttu-id="af5f1-121">Cela facilite la localisation de votre programme en vue de son utilisation dans un autre langage.</span><span class="sxs-lookup"><span data-stu-id="af5f1-121">This makes it easier to localize your program for use with another language.</span></span>

## <a name="requirements"></a><span data-ttu-id="af5f1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af5f1-122">Requirements</span></span>



| <span data-ttu-id="af5f1-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af5f1-123">Requirement</span></span> | <span data-ttu-id="af5f1-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="af5f1-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="af5f1-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af5f1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="af5f1-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af5f1-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="af5f1-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af5f1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="af5f1-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af5f1-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="af5f1-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="af5f1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="af5f1-130"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="af5f1-130"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="af5f1-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af5f1-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="af5f1-132"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af5f1-132"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="af5f1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="af5f1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af5f1-134"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af5f1-134"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af5f1-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af5f1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af5f1-136">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="af5f1-136">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="af5f1-137">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="af5f1-137">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="af5f1-138">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="af5f1-138">*gluQuadricCallback*</span></span>](gluquadric.md)
</dt> <dt>

[<span data-ttu-id="af5f1-139">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="af5f1-139">*gluTessCallback*</span></span>](glutess.md)
</dt> </dl>

 

 





