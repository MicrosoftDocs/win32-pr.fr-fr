---
title: gluNurbsCallback, fonction (Glu. h)
description: La fonction gluNurbsCallback définit un rappel pour un objet NURBS B-spline (NURBS) non uniforme.
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback fonction OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512374"
---
# <a name="glunurbscallback-function"></a><span data-ttu-id="75f70-104">gluNurbsCallback fonction)</span><span class="sxs-lookup"><span data-stu-id="75f70-104">gluNurbsCallback function</span></span>

<span data-ttu-id="75f70-105">La fonction **gluNurbsCallback** définit un rappel pour un objet NURBS B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="75f70-105">The **gluNurbsCallback** function defines a callback for a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f70-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75f70-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="75f70-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75f70-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f70-108">*nobj*</span><span class="sxs-lookup"><span data-stu-id="75f70-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="75f70-109">Objet NURBS (créé avec [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="75f70-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="75f70-110">*et*</span><span class="sxs-lookup"><span data-stu-id="75f70-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="75f70-111">Rappel en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="75f70-111">The callback being defined.</span></span> <span data-ttu-id="75f70-112">La seule valeur valide est GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="75f70-112">The only valid value is GLU\_ERROR.</span></span> <span data-ttu-id="75f70-113">La signification de l' \_ erreur Glu signifie que la fonction d’erreur est appelée lorsqu’une erreur est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="75f70-113">The meaning of GLU\_ERROR means that the error function is called when an error is encountered.</span></span> <span data-ttu-id="75f70-114">Son argument unique est de type **GLenum** et indique l’erreur spécifique qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="75f70-114">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="75f70-115">Il y a 37 erreurs propres à NURBS, nommées GLU \_ NURBS \_ ERROR1 à Glu \_ NURBS \_ ERROR37.</span><span class="sxs-lookup"><span data-stu-id="75f70-115">There are 37 errors unique to NURBS, named GLU\_NURBS\_ERROR1 through GLU\_NURBS\_ERROR37.</span></span> <span data-ttu-id="75f70-116">Les chaînes de caractères décrivant ces erreurs peuvent être récupérées avec [**gluErrorString**](gluerrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="75f70-116">Character strings describing these errors can be retrieved with [**gluErrorString**](gluerrorstring.md).</span></span>

</dd> <dt>

<span data-ttu-id="75f70-117">*FN*</span><span class="sxs-lookup"><span data-stu-id="75f70-117">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="75f70-118">Pointeur vers la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="75f70-118">A pointer to the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f70-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75f70-119">Return value</span></span>

<span data-ttu-id="75f70-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="75f70-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f70-121">Notes</span><span class="sxs-lookup"><span data-stu-id="75f70-121">Remarks</span></span>

<span data-ttu-id="75f70-122">Utilisez **gluNurbsCallback** pour définir un rappel devant être utilisé par un objet NURBS.</span><span class="sxs-lookup"><span data-stu-id="75f70-122">Use **gluNurbsCallback** to define a callback to be used by a NURBS object.</span></span> <span data-ttu-id="75f70-123">Si le rappel spécifié est déjà défini, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="75f70-123">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="75f70-124">Si *FN* a la **valeur null**, tout rappel existant est effacé.</span><span class="sxs-lookup"><span data-stu-id="75f70-124">If *fn* is **NULL**, then any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f70-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75f70-125">Requirements</span></span>



| <span data-ttu-id="75f70-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75f70-126">Requirement</span></span> | <span data-ttu-id="75f70-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="75f70-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75f70-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75f70-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75f70-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75f70-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="75f70-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75f70-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75f70-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75f70-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75f70-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="75f70-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="75f70-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="75f70-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="75f70-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="75f70-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="75f70-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75f70-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="75f70-136">DLL</span><span class="sxs-lookup"><span data-stu-id="75f70-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75f70-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75f70-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f70-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75f70-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f70-139">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="75f70-139">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="75f70-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="75f70-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> </dl>

 

 





