---
title: fonction glTexCoord4dv (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord4dv (GL. h)
ms.assetid: 43d3fb1c-c1cf-4f81-aac2-24a5b4c5b29d
keywords:
- glTexCoord4dv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b2ffb9f14ad0827ff37e4dd057892eb5abea8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522307"
---
# <a name="gltexcoord4dv-function"></a><span data-ttu-id="217e7-105">glTexCoord4dv fonction)</span><span class="sxs-lookup"><span data-stu-id="217e7-105">glTexCoord4dv function</span></span>

<span data-ttu-id="217e7-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="217e7-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="217e7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="217e7-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="217e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="217e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217e7-109">*v*</span><span class="sxs-lookup"><span data-stu-id="217e7-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="217e7-110">Pointeur vers un tableau de quatre éléments, qui à son tour spécifie les coordonnées de texture s, t, r et q.</span><span class="sxs-lookup"><span data-stu-id="217e7-110">A pointer to an array of four elements, which in turn specifies the s, t, r, and q texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217e7-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="217e7-111">Return value</span></span>

<span data-ttu-id="217e7-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="217e7-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="217e7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="217e7-113">Remarks</span></span>

<span data-ttu-id="217e7-114">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="217e7-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="217e7-115">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="217e7-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="217e7-116">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="217e7-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="217e7-117">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="217e7-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="217e7-118">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="217e7-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="217e7-119">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="217e7-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="217e7-120">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="217e7-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="217e7-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="217e7-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="217e7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="217e7-122">Requirements</span></span>



| <span data-ttu-id="217e7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="217e7-123">Requirement</span></span> | <span data-ttu-id="217e7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="217e7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="217e7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="217e7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="217e7-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="217e7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="217e7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="217e7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="217e7-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="217e7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="217e7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="217e7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="217e7-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="217e7-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="217e7-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="217e7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="217e7-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="217e7-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="217e7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="217e7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="217e7-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="217e7-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="217e7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="217e7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217e7-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="217e7-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





