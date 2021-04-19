---
title: fonction glTexCoord2i (GL. h)
description: Définit les coordonnées de texture actuelles. | fonction glTexCoord2i (GL. h)
ms.assetid: 7a5ff9a7-8dcd-47a0-868c-3909e011a592
keywords:
- glTexCoord2i fonction OpenGL
topic_type:
- apiref
api_name:
- glTexCoord2i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa4d710f49d55e8aa0379bfc83f79f877d3cc906
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106536437"
---
# <a name="gltexcoord2i-function"></a><span data-ttu-id="2c6ea-105">glTexCoord2i fonction)</span><span class="sxs-lookup"><span data-stu-id="2c6ea-105">glTexCoord2i function</span></span>

<span data-ttu-id="2c6ea-106">Définit les coordonnées de texture actuelles.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-106">Sets the current texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c6ea-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c6ea-107">Syntax</span></span>


```C++
void WINAPI glTexCoord2i(
   GLint s,
   GLint t
);
```



## <a name="parameters"></a><span data-ttu-id="2c6ea-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c6ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c6ea-109">*s*</span><span class="sxs-lookup"><span data-stu-id="2c6ea-109">*s*</span></span> 
</dt> <dd>

<span data-ttu-id="2c6ea-110">Coordonnée de texture s.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-110">The s texture coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="2c6ea-111">*t*</span><span class="sxs-lookup"><span data-stu-id="2c6ea-111">*t*</span></span> 
</dt> <dd>

<span data-ttu-id="2c6ea-112">Coordonnée de la texture t.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-112">The t texture coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c6ea-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2c6ea-113">Return value</span></span>

<span data-ttu-id="2c6ea-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c6ea-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2c6ea-115">Remarks</span></span>

<span data-ttu-id="2c6ea-116">La fonction [**glTexCoord**](gltexcoord-functions.md) définit les coordonnées de texture actuelles qui font partie des données associées aux sommets de polygone.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-116">The [**glTexCoord**](gltexcoord-functions.md) function sets the current texture coordinates that are part of the data associated with polygon vertices.</span></span> <span data-ttu-id="2c6ea-117">La fonction **glTexCoord** spécifie des coordonnées de texture en une, deux, trois ou quatre dimensions.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-117">The **glTexCoord** function specifies texture coordinates in one, two, three, or four dimensions.</span></span> <span data-ttu-id="2c6ea-118">La fonction glTexCoord1 définit les coordonnées de texture actuelles sur (s, 0, 0, 1); un appel à glTexCoord2 les affecte à la valeur (s, t, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="2c6ea-118">The glTexCoord1 function sets the current texture coordinates to (s, 0, 0, 1); a call to glTexCoord2 sets them to (s, t, 0, 1).</span></span> <span data-ttu-id="2c6ea-119">De même, glTexCoord3 spécifie les coordonnées de la texture comme (s, t, r, 1) et glTexCoord4 définit les quatre composants explicitement comme (s, t, r, q).</span><span class="sxs-lookup"><span data-stu-id="2c6ea-119">Similarly, glTexCoord3 specifies the texture coordinates as (s, t, r, 1), and glTexCoord4 defines all four components explicitly as (s, t, r, q).</span></span> <span data-ttu-id="2c6ea-120">Vous pouvez mettre à jour les coordonnées de texture actuelles à tout moment.</span><span class="sxs-lookup"><span data-stu-id="2c6ea-120">You can update the current texture coordinates at any time.</span></span> <span data-ttu-id="2c6ea-121">En particulier, vous pouvez appeler glTexCoord entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2c6ea-121">In particular, you can call glTexCoord between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="2c6ea-122">La fonction suivante récupère des informations relatives à **glTexCoord**:</span><span class="sxs-lookup"><span data-stu-id="2c6ea-122">The following function retrieves information related to **glTexCoord**:</span></span>

<span data-ttu-id="2c6ea-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument de \_ la \_ texture actuelle de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="2c6ea-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_TEXTURE\_COORDS</span></span>

## <a name="requirements"></a><span data-ttu-id="2c6ea-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c6ea-124">Requirements</span></span>



| <span data-ttu-id="2c6ea-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c6ea-125">Requirement</span></span> | <span data-ttu-id="2c6ea-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c6ea-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6ea-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c6ea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6ea-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c6ea-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c6ea-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c6ea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6ea-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c6ea-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c6ea-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c6ea-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c6ea-132"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ea-132"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2c6ea-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c6ea-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c6ea-134"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ea-134"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c6ea-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2c6ea-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c6ea-136"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c6ea-136"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6ea-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c6ea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6ea-138">glVertex</span><span class="sxs-lookup"><span data-stu-id="2c6ea-138">glVertex</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





