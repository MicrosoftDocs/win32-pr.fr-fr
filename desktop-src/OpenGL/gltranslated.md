---
title: fonction glTranslated (GL. h)
description: La fonction glTranslated multiplie la matrice actuelle par une matrice de translation.
ms.assetid: 9f066a92-ee78-44d1-b8f8-0eacde0e1a47
keywords:
- glTranslated fonction OpenGL
topic_type:
- apiref
api_name:
- glTranslated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705c8dd0635294b066897db99c0770b5f6622c75
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106535099"
---
# <a name="gltranslated-function"></a><span data-ttu-id="58662-104">glTranslated fonction)</span><span class="sxs-lookup"><span data-stu-id="58662-104">glTranslated function</span></span>

<span data-ttu-id="58662-105">La fonction **glTranslated** multiplie la matrice actuelle par une matrice de translation.</span><span class="sxs-lookup"><span data-stu-id="58662-105">The **glTranslated** function multiplies the current matrix by a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="58662-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58662-106">Syntax</span></span>


```C++
void WINAPI glTranslated(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="58662-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58662-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58662-108">*x*</span><span class="sxs-lookup"><span data-stu-id="58662-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="58662-109">Coordonnée *x* d’un vecteur de translation.</span><span class="sxs-lookup"><span data-stu-id="58662-109">The *x* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="58662-110">*y*</span><span class="sxs-lookup"><span data-stu-id="58662-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="58662-111">Coordonnée *y* d’un vecteur de translation.</span><span class="sxs-lookup"><span data-stu-id="58662-111">The *y* coordinate of a translation vector.</span></span>

</dd> <dt>

<span data-ttu-id="58662-112">*z*</span><span class="sxs-lookup"><span data-stu-id="58662-112">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="58662-113">Coordonnée *z* d’un vecteur de translation.</span><span class="sxs-lookup"><span data-stu-id="58662-113">The *z* coordinate of a translation vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58662-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58662-114">Return value</span></span>

<span data-ttu-id="58662-115">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="58662-115">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58662-116">Notes</span><span class="sxs-lookup"><span data-stu-id="58662-116">Remarks</span></span>

<span data-ttu-id="58662-117">La fonction **glTranslated** produit la traduction spécifiée par (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="58662-117">The **glTranslated** function produces the translation specified by (*x*, *y*, *z*).</span></span> <span data-ttu-id="58662-118">Le vecteur de translation est utilisé pour calculer une matrice de traduction 4x4 :</span><span class="sxs-lookup"><span data-stu-id="58662-118">The translation vector is used to compute a 4x4 translation matrix:</span></span>

![Diagramme montrant la matrice de translation 4x4 spécifiée par x, y, z.](images/trans01.png)

<span data-ttu-id="58662-120">La matrice actuelle (voir [**glMatrixMode**](glmatrixmode.md)) est multipliée par cette matrice de translation, le produit remplaçant la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="58662-120">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this translation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="58662-121">Autrement dit, si M est la matrice active et que T est la matrice de translation, M est remplacé par M T.</span><span class="sxs-lookup"><span data-stu-id="58662-121">That is, if M is the current matrix and T is the translation matrix, then M is replaced with M T.</span></span>

<span data-ttu-id="58662-122">Si le mode matriciel est GL \_ MODELVIEW ou GL \_ projection, tous les objets dessinés après l’appel de **glTranslated** sont traduits.</span><span class="sxs-lookup"><span data-stu-id="58662-122">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glTranslated** is called are translated.</span></span> <span data-ttu-id="58662-123">Utilisez [**glPushMatrix**](glpushmatrix.md) et **glPopMatrix** pour enregistrer et restaurer le système de coordonnées non traduit.</span><span class="sxs-lookup"><span data-stu-id="58662-123">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the untranslated coordinate system.</span></span>

<span data-ttu-id="58662-124">Les fonctions suivantes récupèrent les informations relatives à [**glTranslated**](gltranslate.md):</span><span class="sxs-lookup"><span data-stu-id="58662-124">The following functions retrieve information related to [**glTranslated**](gltranslate.md):</span></span>

<span data-ttu-id="58662-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument \_ mode de matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="58662-125">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="58662-126">**glGet** avec argument GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="58662-126">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="58662-127">**glGet** avec argument \_ matrice de projection de la comptabilité \_</span><span class="sxs-lookup"><span data-stu-id="58662-127">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="58662-128">matrice de texture **glGet** avec argument GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="58662-128">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="58662-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58662-129">Requirements</span></span>



| <span data-ttu-id="58662-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58662-130">Requirement</span></span> | <span data-ttu-id="58662-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="58662-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58662-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58662-132">Minimum supported client</span></span><br/> | <span data-ttu-id="58662-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58662-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="58662-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58662-134">Minimum supported server</span></span><br/> | <span data-ttu-id="58662-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58662-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="58662-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="58662-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="58662-137"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="58662-137"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="58662-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="58662-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="58662-139"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58662-139"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="58662-140">DLL</span><span class="sxs-lookup"><span data-stu-id="58662-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58662-141"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58662-141"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58662-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58662-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58662-143">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="58662-143">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="58662-144">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="58662-144">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="58662-145">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="58662-145">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="58662-146">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="58662-146">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="58662-147">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="58662-147">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="58662-148">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="58662-148">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="58662-149">**glScale**</span><span class="sxs-lookup"><span data-stu-id="58662-149">**glScale**</span></span>](glscale.md)
</dt> </dl>

 

 





