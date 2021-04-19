---
title: fonction glGetPointerv (GL. h)
description: La fonction glGetPointerv retourne l’adresse d’un tableau de données de vertex.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- glGetPointerv fonction OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543056"
---
# <a name="glgetpointerv-function"></a><span data-ttu-id="ead33-104">glGetPointerv fonction)</span><span class="sxs-lookup"><span data-stu-id="ead33-104">glGetPointerv function</span></span>

<span data-ttu-id="ead33-105">La fonction **glGetPointerv** retourne l’adresse d’un tableau de données de vertex.</span><span class="sxs-lookup"><span data-stu-id="ead33-105">The **glGetPointerv** function returns the address of a vertex data array.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead33-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ead33-106">Syntax</span></span>


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a><span data-ttu-id="ead33-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ead33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead33-108">*pname*</span><span class="sxs-lookup"><span data-stu-id="ead33-108">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="ead33-109">Type de pointeur de tableau à retourner à partir des constantes symboliques suivantes : pointeur de tableau de couleur de GL, pointeur de tableau d' \_ indicateurs de périphérie du GL, pointeur de \_ tampon de \_ \_ \_ \_ \_ \_ Commentaires GL \_ \_ , pointeur de tableau d' \_ index GL \_ \_ , pointeur de tableau de GL normal, pointeur de tableau de coordonnées de la comptabilité GL, pointeur de \_ \_ tampon de \_ \_ \_ \_ \_ \_ sélection GL \_ \_ et \_ pointeur de tableau de vertex GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ead33-109">The type of array pointer to return from the following symbolic constants: GL\_COLOR\_ARRAY\_POINTER, GL\_EDGE\_FLAG\_ARRAY\_POINTER, GL\_FEEDBACK\_BUFFER\_POINTER, GL\_INDEX\_ARRAY\_POINTER, GL\_NORMAL\_ARRAY\_POINTER, GL\_TEXTURE\_COORD\_ARRAY\_POINTER, GL\_SELECTION\_BUFFER\_POINTER, and GL\_VERTEX\_ARRAY\_POINTER.</span></span>

</dd> <dt>

<span data-ttu-id="ead33-110">*params*</span><span class="sxs-lookup"><span data-stu-id="ead33-110">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="ead33-111">Retourne la valeur du pointeur de tableau spécifié par *pname*.</span><span class="sxs-lookup"><span data-stu-id="ead33-111">Returns the value of the array pointer specified by *pname*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead33-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ead33-112">Return value</span></span>

<span data-ttu-id="ead33-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ead33-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ead33-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ead33-114">Error codes</span></span>

<span data-ttu-id="ead33-115">Le code d’erreur suivant peut être récupéré par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ead33-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ead33-116">Nom</span><span class="sxs-lookup"><span data-stu-id="ead33-116">Name</span></span>                                                                                             | <span data-ttu-id="ead33-117">Signification</span><span class="sxs-lookup"><span data-stu-id="ead33-117">Meaning</span></span>                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="ead33-118"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ead33-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl> | <span data-ttu-id="ead33-119">*pname* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="ead33-119">*pname* was not an accepted value.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ead33-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ead33-120">Remarks</span></span>

<span data-ttu-id="ead33-121">La fonction **glGetPointerv** retourne les informations de pointeur de tableau.</span><span class="sxs-lookup"><span data-stu-id="ead33-121">The **glGetPointerv** function returns array pointer information.</span></span> <span data-ttu-id="ead33-122">Le paramètre *pname* est une constante symbolique spécifiant le type de pointeur de tableau à retourner, et *params* est un pointeur vers un emplacement où placer les données retournées.</span><span class="sxs-lookup"><span data-stu-id="ead33-122">The *pname* parameter is a symbolic constant specifying the kind of array pointer to return, and *params* is a pointer to a location to place the returned data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead33-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ead33-123">Requirements</span></span>



| <span data-ttu-id="ead33-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ead33-124">Requirement</span></span> | <span data-ttu-id="ead33-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ead33-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ead33-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ead33-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ead33-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ead33-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ead33-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ead33-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ead33-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ead33-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ead33-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ead33-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead33-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead33-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ead33-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ead33-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ead33-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ead33-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ead33-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ead33-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ead33-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead33-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead33-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ead33-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead33-137">**glArrayElement**</span><span class="sxs-lookup"><span data-stu-id="ead33-137">**glArrayElement**</span></span>](glarrayelement.md)
</dt> <dt>

[<span data-ttu-id="ead33-138">**glColorPointer**</span><span class="sxs-lookup"><span data-stu-id="ead33-138">**glColorPointer**</span></span>](glcolorpointer.md)
</dt> <dt>

[<span data-ttu-id="ead33-139">**glDrawArrays**</span><span class="sxs-lookup"><span data-stu-id="ead33-139">**glDrawArrays**</span></span>](gldrawarrays.md)
</dt> <dt>

[<span data-ttu-id="ead33-140">**glEdgeFlagPointer**</span><span class="sxs-lookup"><span data-stu-id="ead33-140">**glEdgeFlagPointer**</span></span>](gledgeflagpointer.md)
</dt> <dt>

[<span data-ttu-id="ead33-141">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="ead33-141">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="ead33-142">**glIndexPointer**</span><span class="sxs-lookup"><span data-stu-id="ead33-142">**glIndexPointer**</span></span>](glindexpointer.md)
</dt> <dt>

[<span data-ttu-id="ead33-143">**glNormalPointer**</span><span class="sxs-lookup"><span data-stu-id="ead33-143">**glNormalPointer**</span></span>](glnormalpointer.md)
</dt> <dt>

[<span data-ttu-id="ead33-144">**glTexCoordPointer**</span><span class="sxs-lookup"><span data-stu-id="ead33-144">**glTexCoordPointer**</span></span>](gltexcoordpointer.md)
</dt> <dt>

[<span data-ttu-id="ead33-145">**glVertexPointer**</span><span class="sxs-lookup"><span data-stu-id="ead33-145">**glVertexPointer**</span></span>](glvertexpointer.md)
</dt> </dl>

 

 





