---
title: fonction glTexCoord2sv (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord2sv (GL. h)
ms.assetid: c9e0922c-e120-4e80-baf0-8a18cef5d4f9
keywords:
- glTexCoord2sv fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2sv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c63723a5843d0db9e8054ca8d3fdd9d94f95cac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869958"
---
# <a name="gltexcoord2sv-function"></a><span data-ttu-id="c2fc5-105">glTexCoord2sv fonction)</span><span class="sxs-lookup"><span data-stu-id="c2fc5-105">glTexCoord2sv function</span></span>

<span data-ttu-id="c2fc5-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2fc5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2fc5-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2sv(
   const GLshort *v
);
```



## <a name="parameters"></a><span data-ttu-id="c2fc5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2fc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2fc5-109">*v*</span><span class="sxs-lookup"><span data-stu-id="c2fc5-109">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="c2fc5-110">Pointeur vers un tableau de deux éléments, qui à son tour spécifie les coordonnées de texture s et t.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-110">A pointer to an array of two elements, which in turn specifies the s and t texture coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2fc5-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c2fc5-111">Return value</span></span>

<span data-ttu-id="c2fc5-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2fc5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c2fc5-113">Remarks</span></span>

<span data-ttu-id="c2fc5-114">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="c2fc5-115">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="c2fc5-116">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="c2fc5-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="c2fc5-117">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="c2fc5-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="c2fc5-118">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="c2fc5-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="c2fc5-119">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c2fc5-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="c2fc5-120">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="c2fc5-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="c2fc5-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="c2fc5-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="c2fc5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2fc5-122">Requirements</span></span>



| <span data-ttu-id="c2fc5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2fc5-123">Requirement</span></span> | <span data-ttu-id="c2fc5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2fc5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fc5-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2fc5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c2fc5-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2fc5-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2fc5-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2fc5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c2fc5-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2fc5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2fc5-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2fc5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2fc5-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2fc5-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c2fc5-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2fc5-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2fc5-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2fc5-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2fc5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c2fc5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2fc5-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2fc5-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2fc5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2fc5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2fc5-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="c2fc5-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





