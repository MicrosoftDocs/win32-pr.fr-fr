---
title: fonction glFlush (GL. h)
description: La fonction glFlush force l’exécution des fonctions OpenGL en temps fini.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- glFlush fonction OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743876"
---
# <a name="glflush-function"></a><span data-ttu-id="5d560-104">glFlush fonction)</span><span class="sxs-lookup"><span data-stu-id="5d560-104">glFlush function</span></span>

<span data-ttu-id="5d560-105">La fonction **glFlush** force l’exécution des fonctions OpenGL en temps fini.</span><span class="sxs-lookup"><span data-stu-id="5d560-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d560-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d560-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="5d560-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d560-107">Parameters</span></span>

<span data-ttu-id="5d560-108">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5d560-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d560-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d560-109">Return value</span></span>

<span data-ttu-id="5d560-110">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5d560-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5d560-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5d560-111">Error codes</span></span>

<span data-ttu-id="5d560-112">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5d560-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5d560-113">Nom</span><span class="sxs-lookup"><span data-stu-id="5d560-113">Name</span></span>                                                                                                  | <span data-ttu-id="5d560-114">Signification</span><span class="sxs-lookup"><span data-stu-id="5d560-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d560-115"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5d560-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5d560-116">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5d560-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5d560-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5d560-117">Remarks</span></span>

<span data-ttu-id="5d560-118">Les différentes implémentations OpenGL entamponnt des commandes dans différents emplacements, y compris les tampons réseau et l’accélérateur graphique lui-même.</span><span class="sxs-lookup"><span data-stu-id="5d560-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="5d560-119">La fonction **glFlush** vide toutes ces mémoires tampons, ce qui entraîne l’exécution de toutes les commandes émises aussi rapidement qu’elles sont acceptées par le moteur de rendu réel.</span><span class="sxs-lookup"><span data-stu-id="5d560-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="5d560-120">Bien que cette exécution ne puisse pas être effectuée dans un laps de temps donné, elle se termine dans un laps de temps limité.</span><span class="sxs-lookup"><span data-stu-id="5d560-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="5d560-121">Étant donné que tous les programmes OpenGL peuvent être exécutés sur un réseau, ou sur un accélérateur qui met en mémoire tampon des commandes, veillez à appeler **glFlush** dans tous les programmes nécessitant que toutes les commandes précédemment émises soient terminées.</span><span class="sxs-lookup"><span data-stu-id="5d560-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="5d560-122">Par exemple, appelez **glFlush** avant d’attendre une entrée utilisateur qui dépend de l’image générée.</span><span class="sxs-lookup"><span data-stu-id="5d560-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="5d560-123">La fonction **glFlush** peut retourner à tout moment.</span><span class="sxs-lookup"><span data-stu-id="5d560-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="5d560-124">Il n’attend pas que l’exécution de toutes les fonctions OpenGL précédemment émises soit terminée.</span><span class="sxs-lookup"><span data-stu-id="5d560-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d560-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d560-125">Requirements</span></span>



| <span data-ttu-id="5d560-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d560-126">Requirement</span></span> | <span data-ttu-id="5d560-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d560-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d560-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d560-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5d560-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d560-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5d560-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d560-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5d560-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d560-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d560-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d560-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d560-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d560-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5d560-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d560-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d560-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d560-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5d560-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5d560-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d560-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d560-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d560-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d560-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d560-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5d560-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5d560-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="5d560-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5d560-141">**glFinish**</span><span class="sxs-lookup"><span data-stu-id="5d560-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 





