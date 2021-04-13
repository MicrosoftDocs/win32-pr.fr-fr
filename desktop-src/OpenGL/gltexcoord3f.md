---
title: fonction cglTexCoord3f (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction cglTexCoord3f (GL. h)
ms.assetid: 5ff078bb-040f-47c0-9051-69cde14ba259
keywords:
- glTexCoord3f fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2667b3208b0c8b6c9c6bc1a25dd2a63686f8ddaa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322093"
---
# <a name="cgltexcoord3f-function"></a><span data-ttu-id="11eda-105">cglTexCoord3f fonction)</span><span class="sxs-lookup"><span data-stu-id="11eda-105">cglTexCoord3f function</span></span>

<span data-ttu-id="11eda-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="11eda-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="11eda-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11eda-107">Syntax</span></span>


```C++
void WINAPI glTexCoord3f(
   GLfloat s,
   GLfloat t,
   GLfloat r
);
```



## <a name="parameters"></a><span data-ttu-id="11eda-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11eda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11eda-109">*s*</span><span class="sxs-lookup"><span data-stu-id="11eda-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="11eda-110">Coordonnée de texture s.</span><span class="sxs-lookup"><span data-stu-id="11eda-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="11eda-111">*t*</span><span class="sxs-lookup"><span data-stu-id="11eda-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="11eda-112">Coordonnée de la texture t.</span><span class="sxs-lookup"><span data-stu-id="11eda-112">The t texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="11eda-113">*r*</span><span class="sxs-lookup"><span data-stu-id="11eda-113">*r*</span></span> 
</dt> <dd>

<span data-ttu-id="11eda-114">Coordonnée de texture r.</span><span class="sxs-lookup"><span data-stu-id="11eda-114">The r texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11eda-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11eda-115">Return value</span></span>

<span data-ttu-id="11eda-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="11eda-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11eda-117">Notes</span><span class="sxs-lookup"><span data-stu-id="11eda-117">Remarks</span></span>

<span data-ttu-id="11eda-118">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="11eda-118">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="11eda-119">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="11eda-119">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="11eda-120">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="11eda-120">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="11eda-121">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="11eda-121">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="11eda-122">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="11eda-122">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="11eda-123">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="11eda-123">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="11eda-124">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="11eda-124">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="11eda-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="11eda-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="11eda-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11eda-126">Requirements</span></span>



| <span data-ttu-id="11eda-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11eda-127">Requirement</span></span> | <span data-ttu-id="11eda-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="11eda-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11eda-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11eda-129">Minimum supported client</span></span><br/> | <span data-ttu-id="11eda-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11eda-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="11eda-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11eda-131">Minimum supported server</span></span><br/> | <span data-ttu-id="11eda-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11eda-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11eda-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="11eda-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="11eda-134"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11eda-134"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="11eda-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11eda-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="11eda-136"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11eda-136"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11eda-137">DLL</span><span class="sxs-lookup"><span data-stu-id="11eda-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11eda-138"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11eda-138"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11eda-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11eda-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11eda-140">glVertex</span><span class="sxs-lookup"><span data-stu-id="11eda-140">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





