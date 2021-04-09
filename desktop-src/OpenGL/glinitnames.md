---
title: fonction glInitNames (GL. h)
description: La fonction glInitNames initialise la pile de noms.
ms.assetid: 26c134f5-c17c-4637-93b6-5293f316dd6c
keywords:
- glInitNames fonction OpenGL
topic_type:
- apiref
api_name:
- glInitNames
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ebdb9d19f6c88340fd53162febe694e3566408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102944"
---
# <a name="glinitnames-function"></a><span data-ttu-id="c6bcd-104">glInitNames fonction)</span><span class="sxs-lookup"><span data-stu-id="c6bcd-104">glInitNames function</span></span>

<span data-ttu-id="c6bcd-105">La fonction **glInitNames** initialise la pile de noms.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-105">The **glInitNames** function initializes the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6bcd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6bcd-106">Syntax</span></span>


```C++
void WINAPI glInitNames(void);
```



## <a name="parameters"></a><span data-ttu-id="c6bcd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6bcd-107">Parameters</span></span>

<span data-ttu-id="c6bcd-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6bcd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6bcd-109">Return value</span></span>

<span data-ttu-id="c6bcd-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c6bcd-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c6bcd-111">Error codes</span></span>

<span data-ttu-id="c6bcd-112">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c6bcd-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c6bcd-113">Nom</span><span class="sxs-lookup"><span data-stu-id="c6bcd-113">Name</span></span>                                                                                                  | <span data-ttu-id="c6bcd-114">Signification</span><span class="sxs-lookup"><span data-stu-id="c6bcd-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6bcd-115"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c6bcd-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c6bcd-116">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c6bcd-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c6bcd-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c6bcd-117">Remarks</span></span>

<span data-ttu-id="c6bcd-118">La fonction **glInitNames** provoque l’initialisation de la pile de noms à son état vide par défaut.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-118">The **glInitNames** function causes the name stack to be initialized to its default empty state.</span></span> <span data-ttu-id="c6bcd-119">La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-119">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="c6bcd-120">Il se compose d’un ensemble ordonné d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-120">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="c6bcd-121">La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ .</span><span class="sxs-lookup"><span data-stu-id="c6bcd-121">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="c6bcd-122">Les appels à **glInitNames** alors que le mode de rendu n’est pas GL \_ Select sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="c6bcd-122">Calls to **glInitNames** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="c6bcd-123">Les fonctions suivantes récupèrent les informations relatives à **glInitNames**:</span><span class="sxs-lookup"><span data-stu-id="c6bcd-123">The following functions retrieve information related to **glInitNames**:</span></span>

<span data-ttu-id="c6bcd-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="c6bcd-124">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="c6bcd-125">**glGet** avec argument GL \_ Max \_ nom \_ \_ profondeur de la pile</span><span class="sxs-lookup"><span data-stu-id="c6bcd-125">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="c6bcd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6bcd-126">Requirements</span></span>



| <span data-ttu-id="c6bcd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6bcd-127">Requirement</span></span> | <span data-ttu-id="c6bcd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6bcd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6bcd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6bcd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c6bcd-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6bcd-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c6bcd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6bcd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c6bcd-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6bcd-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6bcd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6bcd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6bcd-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6bcd-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c6bcd-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c6bcd-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6bcd-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6bcd-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c6bcd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c6bcd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6bcd-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6bcd-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6bcd-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6bcd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6bcd-140">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c6bcd-140">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c6bcd-141">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c6bcd-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c6bcd-142">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="c6bcd-142">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="c6bcd-143">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="c6bcd-143">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="c6bcd-144">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="c6bcd-144">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="c6bcd-145">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="c6bcd-145">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





