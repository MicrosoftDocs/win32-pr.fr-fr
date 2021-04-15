---
title: fonction glTexCoord1d (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord1d (GL. h)
ms.assetid: 95b76b08-f4db-4b1c-835b-a27cf81c64fb
keywords:
- glTexCoord1d fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29b92314301337b755f15c11ff4717a42aca555c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394028"
---
# <a name="gltexcoord1d-function"></a><span data-ttu-id="98e8f-105">glTexCoord1d fonction)</span><span class="sxs-lookup"><span data-stu-id="98e8f-105">glTexCoord1d function</span></span>

<span data-ttu-id="98e8f-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="98e8f-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98e8f-107">Syntax</span></span>


```C++
void WINAPI glTexCoord1d(
   GLdouble s
);
```



## <a name="parameters"></a><span data-ttu-id="98e8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98e8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e8f-109">*s*</span><span class="sxs-lookup"><span data-stu-id="98e8f-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="98e8f-110">Coordonnée de texture s.</span><span class="sxs-lookup"><span data-stu-id="98e8f-110">The s texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e8f-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="98e8f-111">Return value</span></span>

<span data-ttu-id="98e8f-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="98e8f-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e8f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="98e8f-113">Remarks</span></span>

<span data-ttu-id="98e8f-114">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="98e8f-114">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="98e8f-115">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="98e8f-115">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="98e8f-116">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="98e8f-116">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="98e8f-117">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="98e8f-117">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="98e8f-118">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="98e8f-118">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="98e8f-119">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="98e8f-119">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="98e8f-120">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="98e8f-120">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="98e8f-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="98e8f-121">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="98e8f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98e8f-122">Requirements</span></span>



| <span data-ttu-id="98e8f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98e8f-123">Requirement</span></span> | <span data-ttu-id="98e8f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="98e8f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e8f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98e8f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="98e8f-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98e8f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="98e8f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98e8f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="98e8f-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98e8f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98e8f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="98e8f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e8f-130"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e8f-130"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="98e8f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98e8f-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="98e8f-132"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98e8f-132"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="98e8f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="98e8f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98e8f-134"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e8f-134"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e8f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98e8f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e8f-136">glVertex</span><span class="sxs-lookup"><span data-stu-id="98e8f-136">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





