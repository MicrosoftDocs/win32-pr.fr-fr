---
title: fonction glTexCoord2dv (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord2dv (GL. h)
ms.assetid: e324a5ac-6251-42f8-9483-3d6ad8ae321f
keywords:
- glTexCoord2dv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2dv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee3f9269b4a65c7dcef143506b336c0936209ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106527061"
---
# <a name="gltexcoord2dv-function"></a><span data-ttu-id="be1ca-105">glTexCoord2dv fonction)</span><span class="sxs-lookup"><span data-stu-id="be1ca-105">glTexCoord2dv function</span></span>

<span data-ttu-id="be1ca-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="be1ca-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="be1ca-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be1ca-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2dv(
   const GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="be1ca-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be1ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be1ca-109">*v*</span><span class="sxs-lookup"><span data-stu-id="be1ca-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="be1ca-110">Pointeur vers un tableau de deux éléments, qui à son tour spécifie les coordonnées de texture s et t.</span><span class="sxs-lookup"><span data-stu-id="be1ca-110">A pointer to an array of two elements, which in turn specifies the s and t texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be1ca-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be1ca-111">Return value</span></span>

<span data-ttu-id="be1ca-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="be1ca-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1ca-113">Notes</span><span class="sxs-lookup"><span data-stu-id="be1ca-113">Remarks</span></span>

<span data-ttu-id="be1ca-114">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="be1ca-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="be1ca-115">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="be1ca-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="be1ca-116">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="be1ca-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="be1ca-117">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="be1ca-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="be1ca-118">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="be1ca-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="be1ca-119">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="be1ca-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="be1ca-120">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="be1ca-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="be1ca-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="be1ca-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="be1ca-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be1ca-122">Requirements</span></span>



| <span data-ttu-id="be1ca-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be1ca-123">Requirement</span></span> | <span data-ttu-id="be1ca-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="be1ca-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be1ca-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be1ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be1ca-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be1ca-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="be1ca-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be1ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be1ca-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be1ca-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be1ca-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="be1ca-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be1ca-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="be1ca-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="be1ca-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be1ca-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="be1ca-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be1ca-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="be1ca-133">DLL</span><span class="sxs-lookup"><span data-stu-id="be1ca-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be1ca-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be1ca-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be1ca-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be1ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be1ca-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="be1ca-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





