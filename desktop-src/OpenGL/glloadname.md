---
title: fonction glLoadName (GL. h)
description: La fonction glLoadName charge un nom dans la pile de noms.
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glLoadName fonction OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb47a0389cda13523104ee429bca46838970e15a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106411"
---
# <a name="glloadname-function"></a><span data-ttu-id="939a8-104">glLoadName fonction)</span><span class="sxs-lookup"><span data-stu-id="939a8-104">glLoadName function</span></span>

<span data-ttu-id="939a8-105">La fonction **glLoadName** charge un nom dans la pile de noms.</span><span class="sxs-lookup"><span data-stu-id="939a8-105">The **glLoadName** function loads a name onto the name stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="939a8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="939a8-106">Syntax</span></span>


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a><span data-ttu-id="939a8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="939a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="939a8-108">*name*</span><span class="sxs-lookup"><span data-stu-id="939a8-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="939a8-109">Nom qui remplacera la valeur supérieure de la pile de noms.</span><span class="sxs-lookup"><span data-stu-id="939a8-109">A name that will replace the top value on the name stack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="939a8-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="939a8-110">Return value</span></span>

<span data-ttu-id="939a8-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="939a8-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="939a8-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="939a8-112">Error codes</span></span>

<span data-ttu-id="939a8-113">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="939a8-113">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="939a8-114">Nom</span><span class="sxs-lookup"><span data-stu-id="939a8-114">Name</span></span>                                                                                                  | <span data-ttu-id="939a8-115">Signification</span><span class="sxs-lookup"><span data-stu-id="939a8-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="939a8-116"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="939a8-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="939a8-117">La fonction a été appelée alors que la pile de noms était vide.</span><span class="sxs-lookup"><span data-stu-id="939a8-117">The function was called while the name stack was empty.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="939a8-118"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="939a8-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="939a8-119">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="939a8-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="939a8-120">Notes</span><span class="sxs-lookup"><span data-stu-id="939a8-120">Remarks</span></span>

<span data-ttu-id="939a8-121">La fonction **glLoadName** fait en sorte que *Name* remplace la valeur en haut de la pile de noms, qui est initialement vide.</span><span class="sxs-lookup"><span data-stu-id="939a8-121">The **glLoadName** function causes *name* to replace the value on the top of the name stack, which is initially empty.</span></span> <span data-ttu-id="939a8-122">La pile de noms est utilisée en mode de sélection pour permettre l’identification unique des jeux de commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="939a8-122">The name stack is used during selection mode to allow sets of rendering commands to be uniquely identified.</span></span> <span data-ttu-id="939a8-123">Il se compose d’un ensemble ordonné d’entiers non signés.</span><span class="sxs-lookup"><span data-stu-id="939a8-123">It consists of an ordered set of unsigned integers.</span></span>

<span data-ttu-id="939a8-124">La pile de noms est toujours vide lorsque le mode de rendu n’est pas la sélection de la comptabilité \_ .</span><span class="sxs-lookup"><span data-stu-id="939a8-124">The name stack is always empty while the render mode is not GL\_SELECT.</span></span> <span data-ttu-id="939a8-125">Les appels à **glLoadName** alors que le mode de rendu n’est pas GL \_ Select sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="939a8-125">Calls to **glLoadName** while the render mode is not GL\_SELECT are ignored.</span></span>

<span data-ttu-id="939a8-126">Les fonctions suivantes récupèrent les informations relatives à **glLoadName**:</span><span class="sxs-lookup"><span data-stu-id="939a8-126">The following functions retrieve information related to **glLoadName**:</span></span>

<span data-ttu-id="939a8-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de la profondeur de la \_ pile nom GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="939a8-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

<span data-ttu-id="939a8-128">**glGet** avec argument GL \_ Max \_ nom \_ \_ profondeur de la pile</span><span class="sxs-lookup"><span data-stu-id="939a8-128">**glGet** with argument GL\_MAX\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="939a8-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="939a8-129">Requirements</span></span>



| <span data-ttu-id="939a8-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="939a8-130">Requirement</span></span> | <span data-ttu-id="939a8-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="939a8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="939a8-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="939a8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="939a8-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="939a8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="939a8-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="939a8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="939a8-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="939a8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="939a8-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="939a8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="939a8-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="939a8-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="939a8-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="939a8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="939a8-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="939a8-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="939a8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="939a8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="939a8-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="939a8-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="939a8-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="939a8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939a8-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="939a8-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="939a8-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="939a8-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="939a8-145">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="939a8-145">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="939a8-146">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="939a8-146">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="939a8-147">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="939a8-147">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="939a8-148">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="939a8-148">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





