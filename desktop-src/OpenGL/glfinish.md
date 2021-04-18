---
title: fonction glFinish (GL. h)
description: La fonction glFinish se bloque jusqu’à ce que toute l’exécution de OpenGL soit terminée.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- glFinish fonction OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519154"
---
# <a name="glfinish-function"></a><span data-ttu-id="f7e11-104">glFinish fonction)</span><span class="sxs-lookup"><span data-stu-id="f7e11-104">glFinish function</span></span>

<span data-ttu-id="f7e11-105">La fonction **glFinish** se bloque jusqu’à ce que toute l’exécution de OpenGL soit terminée.</span><span class="sxs-lookup"><span data-stu-id="f7e11-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e11-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7e11-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="f7e11-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7e11-107">Parameters</span></span>

<span data-ttu-id="f7e11-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f7e11-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7e11-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7e11-109">Return value</span></span>

<span data-ttu-id="f7e11-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f7e11-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7e11-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f7e11-111">Error codes</span></span>

<span data-ttu-id="f7e11-112">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f7e11-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f7e11-113">Nom</span><span class="sxs-lookup"><span data-stu-id="f7e11-113">Name</span></span>                                                                                                  | <span data-ttu-id="f7e11-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f7e11-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7e11-115"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f7e11-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f7e11-116">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f7e11-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f7e11-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f7e11-117">Remarks</span></span>

<span data-ttu-id="f7e11-118">La fonction **glFinish** ne retourne pas de résultat tant que les effets de toutes les fonctions OpenGL appelées précédemment ne sont pas terminés.</span><span class="sxs-lookup"><span data-stu-id="f7e11-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="f7e11-119">Ces effets incluent toutes les modifications apportées à l’État OpenGL, toutes les modifications apportées à l’état de la connexion et toutes les modifications apportées au contenu de trame.</span><span class="sxs-lookup"><span data-stu-id="f7e11-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="f7e11-120">La fonction **glFinish** nécessite un aller-retour au serveur.</span><span class="sxs-lookup"><span data-stu-id="f7e11-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e11-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7e11-121">Requirements</span></span>



| <span data-ttu-id="f7e11-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7e11-122">Requirement</span></span> | <span data-ttu-id="f7e11-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7e11-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e11-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7e11-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e11-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7e11-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f7e11-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7e11-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e11-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7e11-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7e11-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7e11-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e11-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7e11-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f7e11-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7e11-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7e11-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7e11-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f7e11-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f7e11-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7e11-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7e11-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e11-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7e11-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e11-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f7e11-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f7e11-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f7e11-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f7e11-137">**glFlush**</span><span class="sxs-lookup"><span data-stu-id="f7e11-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





