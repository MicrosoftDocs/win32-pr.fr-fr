---
title: fonction glGetColorTableParameterivEXT (GL. h)
description: Les fonctions glGetColorTableParameterfvEXT et glGetColorTableParameterivEXT obtiennent des paramètres de palette à partir des tables de couleurs. | fonction glGetColorTableParameterivEXT (GL. h)
ms.assetid: 39a0b346-d103-4426-8536-95e7e1548f7a
keywords:
- glGetColorTableParameterivEXT fonction OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterivEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897dd11781968838bb8c26a716e3857acc119e9c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106524825"
---
# <a name="glgetcolortableparameterivext-function"></a><span data-ttu-id="0f148-105">glGetColorTableParameterivEXT fonction)</span><span class="sxs-lookup"><span data-stu-id="0f148-105">glGetColorTableParameterivEXT function</span></span>

<span data-ttu-id="0f148-106">Les fonctions [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) et **glGetColorTableParameterivEXT** obtiennent des paramètres de palette à partir des tables de couleurs.</span><span class="sxs-lookup"><span data-stu-id="0f148-106">The [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) and **glGetColorTableParameterivEXT** functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f148-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f148-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterivEXT(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="0f148-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f148-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f148-109">*cible*</span><span class="sxs-lookup"><span data-stu-id="0f148-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="0f148-110">Texture cible de la palette pour laquelle vous souhaitez obtenir des données de paramètre.</span><span class="sxs-lookup"><span data-stu-id="0f148-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="0f148-111">Doit être une TEXTURE \_ 1D, une texture \_ 2D, une texture de proxy \_ \_ 1D ou une texture de proxy \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="0f148-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="0f148-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="0f148-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="0f148-113">Constante symbolique pour le type de données de paramètre de palette vers lequel pointe les *paramètres.*</span><span class="sxs-lookup"><span data-stu-id="0f148-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="0f148-114">Voici les constantes symboliques acceptées et leurs significations.</span><span class="sxs-lookup"><span data-stu-id="0f148-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="0f148-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f148-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="0f148-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0f148-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="0f148-117"><dt>**\_format de table de couleurs GL \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="0f148-118">Retourne le format interne spécifié par l’appel le plus récent à [**glColorTableEXT**](glcolortableext.md) ou la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0f148-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="0f148-119"><dt>**\_largeur de table de couleur GL \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="0f148-120">Retourne la largeur de la palette actuelle.</span><span class="sxs-lookup"><span data-stu-id="0f148-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="0f148-121"><dt>**Table des couleurs GL- \_ \_ \_ \_ taille rouge \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="0f148-122">Retourne la taille réelle utilisée en interne pour stocker le composant rouge des données de la palette.</span><span class="sxs-lookup"><span data-stu-id="0f148-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="0f148-123"><dt>**taille de la table de couleur GL- \_ \_ \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="0f148-124">Retourne la taille réelle utilisée en interne pour stocker le composant vert des données de la palette.</span><span class="sxs-lookup"><span data-stu-id="0f148-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="0f148-125"><dt>**taille de la table de couleur GL en \_ \_ \_ bleu \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="0f148-126">Retourne la taille réelle utilisée en interne pour stocker le composant bleu des données de palette.</span><span class="sxs-lookup"><span data-stu-id="0f148-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="0f148-127"><dt>**Table des couleurs GL- \_ \_ \_ \_ taille alpha \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="0f148-128">Retourne la taille réelle utilisée en interne pour stocker le composant alpha des données de palette.</span><span class="sxs-lookup"><span data-stu-id="0f148-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="0f148-129">*params*</span><span class="sxs-lookup"><span data-stu-id="0f148-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="0f148-130">Pointe vers les données de paramètre de table de couleurs spécifiées par le paramètre *pname* .</span><span class="sxs-lookup"><span data-stu-id="0f148-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f148-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0f148-131">Return value</span></span>

<span data-ttu-id="0f148-132">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0f148-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f148-133">Notes</span><span class="sxs-lookup"><span data-stu-id="0f148-133">Remarks</span></span>

<span data-ttu-id="0f148-134">Vous utilisez les fonctions **glGetColorTableParameterivEXT** et [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) pour récupérer des données de paramètres spécifiques à partir de tables de couleurs définies avec [**glColorTableEXT**](glcolortableext.md) pour les palettes de texture ciblées.</span><span class="sxs-lookup"><span data-stu-id="0f148-134">You use the **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="0f148-135">Vous pouvez également utiliser ces fonctions pour déterminer le nombre d’entrées de table des couleurs retournées par **glGetColorTableEXT** .</span><span class="sxs-lookup"><span data-stu-id="0f148-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="0f148-136">Lorsque le paramètre *cible* est \_ une texture \_ de proxy de GL \_ 1D ou \_ une texture de proxy GL \_ \_ 2D, et que l’implémentation ne prend pas en charge les valeurs spécifiées pour le *format* ou la *largeur*, **glColorTableEXT** peut ne pas réussir à créer la table de couleurs demandée.</span><span class="sxs-lookup"><span data-stu-id="0f148-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="0f148-137">Dans ce cas, la table des couleurs est vide et tous les paramètres récupérés sont nuls.</span><span class="sxs-lookup"><span data-stu-id="0f148-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="0f148-138">Vous pouvez déterminer si OpenGL prend en charge un format et une taille de table de couleur particuliers en appelant **glColorTableEXT** avec une cible de proxy, puis en appelant **glGetColorTableParameterivEXT** ou [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) pour déterminer si le paramètre Width correspond à celui défini par **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="0f148-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="0f148-139">Si la largeur Récupérée est égale à zéro, la requête de la table de couleurs par **glColorTable** a échoué.</span><span class="sxs-lookup"><span data-stu-id="0f148-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="0f148-140">Si la largeur Récupérée n’est pas égale à zéro, vous pouvez appeler **glColorTable** avec la cible réelle avec la texture \_ 1D ou texture \_ 2D pour définir la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="0f148-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="0f148-141">Les fonctions **glGetColorTableParameterivEXT** et [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) sont des fonctions d’extension qui ne font pas partie de la bibliothèque OpenGL standard, mais font partie de l’extension de \_ texture de palette ext GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0f148-141">The **glGetColorTableParameterivEXT** and [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="0f148-142">Pour vérifier si votre implémentation de OpenGL prend en charge **glGetColorTableParameterivEXT** et **glGetColorTableParameterfvEXT**, appelez [**glGetString**](glgetstring.md)**(** \_ Extensions GL **)**.</span><span class="sxs-lookup"><span data-stu-id="0f148-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="0f148-143">Si elle retourne la \_ texture de palette ext GL \_ \_ , **glGetColorTableParameterivEXT** et **glGetColorTableParameterfvEXT** sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0f148-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="0f148-144">Pour obtenir l’adresse de fonction d’une fonction d’extension, appelez [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0f148-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f148-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f148-145">Requirements</span></span>



| <span data-ttu-id="0f148-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f148-146">Requirement</span></span> | <span data-ttu-id="0f148-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f148-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0f148-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f148-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0f148-149">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f148-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="0f148-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f148-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0f148-151">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f148-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0f148-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f148-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f148-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f148-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f148-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f148-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f148-155">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="0f148-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="0f148-156">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="0f148-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="0f148-157">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="0f148-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="0f148-158">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="0f148-158">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="0f148-159">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="0f148-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





