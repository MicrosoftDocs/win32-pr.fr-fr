---
title: fonction glTexCoord2d (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord2d (GL. h)
ms.assetid: 624d566f-72ae-4a7d-adad-5fcfee5b5aca
keywords:
- glTexCoord2d fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 825df8eb8adbfca08b11620d74928284a613780b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543013"
---
# <a name="gltexcoord2d-function"></a><span data-ttu-id="086f2-105">glTexCoord2d fonction)</span><span class="sxs-lookup"><span data-stu-id="086f2-105">glTexCoord2d function</span></span>

<span data-ttu-id="086f2-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="086f2-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="086f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="086f2-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2d(
   GLdouble s,
   GLdouble t
);
```



## <a name="parameters"></a><span data-ttu-id="086f2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="086f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="086f2-109">*s*</span><span class="sxs-lookup"><span data-stu-id="086f2-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="086f2-110">Coordonnée de texture s.</span><span class="sxs-lookup"><span data-stu-id="086f2-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="086f2-111">*t*</span><span class="sxs-lookup"><span data-stu-id="086f2-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="086f2-112">Coordonnée de la texture t.</span><span class="sxs-lookup"><span data-stu-id="086f2-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="086f2-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="086f2-113">Return value</span></span>

<span data-ttu-id="086f2-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="086f2-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="086f2-115">Notes</span><span class="sxs-lookup"><span data-stu-id="086f2-115">Remarks</span></span>

<span data-ttu-id="086f2-116">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="086f2-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="086f2-117">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="086f2-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="086f2-118">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="086f2-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="086f2-119">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="086f2-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="086f2-120">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="086f2-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="086f2-121">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="086f2-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="086f2-122">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="086f2-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="086f2-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="086f2-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="086f2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="086f2-124">Requirements</span></span>



| <span data-ttu-id="086f2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="086f2-125">Requirement</span></span> | <span data-ttu-id="086f2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="086f2-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="086f2-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="086f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="086f2-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="086f2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="086f2-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="086f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="086f2-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="086f2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="086f2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="086f2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="086f2-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="086f2-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="086f2-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="086f2-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="086f2-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="086f2-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="086f2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="086f2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="086f2-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="086f2-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="086f2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="086f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086f2-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="086f2-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





