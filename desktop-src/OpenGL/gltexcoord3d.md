---
title: fonction glTexCoord3d (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord3d (GL. h)
ms.assetid: 41b8aa69-c069-493f-a1e3-51cf6a01209e
keywords:
- glTexCoord3d fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb7603ed0f823e3b8d841328378d9e207638716
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530742"
---
# <a name="gltexcoord3d-function"></a><span data-ttu-id="6a987-105">glTexCoord3d fonction)</span><span class="sxs-lookup"><span data-stu-id="6a987-105">glTexCoord3d function</span></span>

<span data-ttu-id="6a987-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="6a987-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a987-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a987-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3d(
   GLdouble s,
   GLdouble t,
   GLdouble r
);
```



## <a name="parameters"></a><span data-ttu-id="6a987-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a987-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a987-109">*s*</span><span class="sxs-lookup"><span data-stu-id="6a987-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="6a987-110">Coordonnée de texture s.</span><span class="sxs-lookup"><span data-stu-id="6a987-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6a987-111">*t*</span><span class="sxs-lookup"><span data-stu-id="6a987-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="6a987-112">Coordonnée de la texture t.</span><span class="sxs-lookup"><span data-stu-id="6a987-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6a987-113">*r*</span><span class="sxs-lookup"><span data-stu-id="6a987-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="6a987-114">Coordonnée de texture r.</span><span class="sxs-lookup"><span data-stu-id="6a987-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a987-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a987-115">Return value</span></span>

<span data-ttu-id="6a987-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6a987-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a987-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6a987-117">Remarks</span></span>

<span data-ttu-id="6a987-118">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="6a987-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="6a987-119">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="6a987-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="6a987-120">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="6a987-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="6a987-121">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="6a987-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="6a987-122">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="6a987-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="6a987-123">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6a987-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="6a987-124">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="6a987-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="6a987-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="6a987-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="6a987-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a987-126">Requirements</span></span>



| <span data-ttu-id="6a987-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a987-127">Requirement</span></span> | <span data-ttu-id="6a987-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a987-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a987-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a987-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a987-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a987-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6a987-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a987-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a987-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a987-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a987-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a987-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a987-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a987-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6a987-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a987-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a987-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a987-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6a987-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6a987-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a987-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a987-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a987-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a987-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a987-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="6a987-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





