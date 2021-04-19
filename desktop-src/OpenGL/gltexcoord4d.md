---
title: fonction glTexCoord4d (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord4d (GL. h)
ms.assetid: d9045a2e-81f3-4f63-8eee-e882c586b8fe
keywords:
- glTexCoord4d fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6671b5eee2fab966438075d56de1da2ca4537793
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535146"
---
# <a name="gltexcoord4d-function"></a><span data-ttu-id="d4700-105">glTexCoord4d fonction)</span><span class="sxs-lookup"><span data-stu-id="d4700-105">glTexCoord4d function</span></span>

<span data-ttu-id="d4700-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="d4700-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4700-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4700-107">Syntax</span></span>


```C++
void WINAPI glTexCoord4d(
   GLdouble s,
   GLdouble t,
   GLdouble r,
   GLdouble q
);
```



## <a name="parameters"></a><span data-ttu-id="d4700-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4700-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4700-109">*s*</span><span class="sxs-lookup"><span data-stu-id="d4700-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="d4700-110">Coordonnée de texture s.</span><span class="sxs-lookup"><span data-stu-id="d4700-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="d4700-111">*t*</span><span class="sxs-lookup"><span data-stu-id="d4700-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="d4700-112">Coordonnée de la texture t.</span><span class="sxs-lookup"><span data-stu-id="d4700-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="d4700-113">*r*</span><span class="sxs-lookup"><span data-stu-id="d4700-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="d4700-114">Coordonnée de texture r.</span><span class="sxs-lookup"><span data-stu-id="d4700-114">The r texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="d4700-115">*question*</span><span class="sxs-lookup"><span data-stu-id="d4700-115">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="d4700-116">Coordonnée de texture q.</span><span class="sxs-lookup"><span data-stu-id="d4700-116">The q texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4700-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4700-117">Return value</span></span>

<span data-ttu-id="d4700-118">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d4700-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4700-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d4700-119">Remarks</span></span>

<span data-ttu-id="d4700-120">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="d4700-120">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="d4700-121">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="d4700-121">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="d4700-122">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="d4700-122">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="d4700-123">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="d4700-123">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="d4700-124">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d4700-124">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="d4700-125">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d4700-125">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="d4700-126">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="d4700-126">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="d4700-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="d4700-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="d4700-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4700-128">Requirements</span></span>



| <span data-ttu-id="d4700-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4700-129">Requirement</span></span> | <span data-ttu-id="d4700-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4700-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4700-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4700-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d4700-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4700-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d4700-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4700-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d4700-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4700-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d4700-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4700-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4700-136"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4700-136"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d4700-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4700-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4700-138"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4700-138"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d4700-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d4700-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4700-140"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4700-140"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4700-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4700-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4700-142">glVertex</span><span class="sxs-lookup"><span data-stu-id="d4700-142">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





