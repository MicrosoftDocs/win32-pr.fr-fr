---
title: fonction glFeedbackBuffer (GL. h)
description: La fonction glFeedbackBuffer contrôle le mode de feedback.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer fonction OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512586"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="76a96-104">glFeedbackBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="76a96-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="76a96-105">La fonction **glFeedbackBuffer** contrôle le mode de feedback.</span><span class="sxs-lookup"><span data-stu-id="76a96-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a96-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76a96-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="76a96-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76a96-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a96-108">*size*</span><span class="sxs-lookup"><span data-stu-id="76a96-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="76a96-109">Nombre maximal de valeurs qui peuvent être écrites dans la *mémoire tampon*.</span><span class="sxs-lookup"><span data-stu-id="76a96-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="76a96-110">*type*</span><span class="sxs-lookup"><span data-stu-id="76a96-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="76a96-111">Constante symbolique qui décrit les informations qui seront retournées pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="76a96-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="76a96-112">Les constantes symboliques suivantes sont acceptées : GL \_ 2D, GL \_ 3D, GL \_ 3D \_ Color, GL \_ 3D texture Color \_ \_ et GL \_ 4D \_ Color \_ texture.</span><span class="sxs-lookup"><span data-stu-id="76a96-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="76a96-113">*mémoire tampon*</span><span class="sxs-lookup"><span data-stu-id="76a96-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="76a96-114">Retourne les données de commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76a96-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="76a96-115">Return value</span></span>

<span data-ttu-id="76a96-116">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="76a96-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="76a96-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="76a96-117">Error codes</span></span>

<span data-ttu-id="76a96-118">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="76a96-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="76a96-119">Nom</span><span class="sxs-lookup"><span data-stu-id="76a96-119">Name</span></span>                                                                                                  | <span data-ttu-id="76a96-120">Signification</span><span class="sxs-lookup"><span data-stu-id="76a96-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="76a96-121"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="76a96-122">le *type* n’est pas une valeur acceptée.</span><span class="sxs-lookup"><span data-stu-id="76a96-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="76a96-123"><dt>**\_enum GL non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="76a96-124">la *taille* était négative.</span><span class="sxs-lookup"><span data-stu-id="76a96-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="76a96-125"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="76a96-126">**glFeedbackBuffer** a été appelé alors que le mode de rendu était \_ Commentaires sur le GL, ou [**glRenderMode**](glrendermode.md) a été appelé avec des commentaires sur l’argument GL \_ avant que **glFeedbackBuffer** n’ait été appelé au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="76a96-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="76a96-127"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="76a96-128">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="76a96-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="76a96-129">Notes</span><span class="sxs-lookup"><span data-stu-id="76a96-129">Remarks</span></span>

<span data-ttu-id="76a96-130">La fonction **glFeedbackBuffer** contrôle les commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="76a96-131">Les commentaires, comme la sélection, sont un mode OpenGL.</span><span class="sxs-lookup"><span data-stu-id="76a96-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="76a96-132">Le mode est sélectionné en appelant [**glRenderMode**](glrendermode.md) avec les commentaires sur le GL \_ .</span><span class="sxs-lookup"><span data-stu-id="76a96-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="76a96-133">Lorsque OpenGL est en mode commentaires, aucun Pixel n’est généré par pixellisation.</span><span class="sxs-lookup"><span data-stu-id="76a96-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="76a96-134">Au lieu de cela, les informations sur les primitives qui auraient été pixellisées sont renvoyées à l’application à l’aide de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="76a96-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="76a96-135">La fonction **glFeedbackBuffer** a trois arguments :</span><span class="sxs-lookup"><span data-stu-id="76a96-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="76a96-136">*buffer* est un pointeur vers un tableau de valeurs à virgule flottante dans lequel les informations de commentaires sont placées.</span><span class="sxs-lookup"><span data-stu-id="76a96-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="76a96-137">*taille* indique la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="76a96-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="76a96-138">le *type* est une constante symbolique décrivant les informations qui sont renvoyées pour chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="76a96-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="76a96-139">Vous devez émettre **glFeedbackBuffer** pour que le mode Commentaires soit activé (en appelant **glRenderMode** avec les commentaires sur l’argument GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="76a96-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="76a96-140">La définition \_ de commentaires sur le GL sans l’établissement de la mémoire tampon de commentaires, ou l’appel de **glFeedbackBuffer** alors que OpenGL est en mode commentaires, est une erreur.</span><span class="sxs-lookup"><span data-stu-id="76a96-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="76a96-141">Veillez à utiliser le mode Feedback en appelant [**glRenderMode**](glrendermode.md) avec une valeur de paramètre autre que le \_ Feedback GL.</span><span class="sxs-lookup"><span data-stu-id="76a96-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="76a96-142">Lorsque vous effectuez cette opération alors que OpenGL est en mode commentaires, **glRenderMode** retourne le nombre d’entrées placées dans le tableau de commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="76a96-143">La valeur retournée n’est jamais supérieure à la *taille*.</span><span class="sxs-lookup"><span data-stu-id="76a96-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="76a96-144">Si les données de commentaires requièrent plus d’espace que ce qui était disponible dans la *mémoire tampon*, **glRenderMode** retourne une valeur négative.</span><span class="sxs-lookup"><span data-stu-id="76a96-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="76a96-145">En mode commentaires, chaque primitive qui serait pixellisée génère un bloc de valeurs copiées dans le tableau de commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="76a96-146">Si vous procédez ainsi, le nombre d’entrées dépasse le maximum, **glFeedbackBuffer** écrit partiellement le bloc afin de remplir le tableau (s’il reste de la place) et définit un indicateur de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="76a96-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="76a96-147">Chaque bloc commence par un code qui indique le type primitif, suivi de valeurs qui décrivent les vertex de la primitive et les données associées.</span><span class="sxs-lookup"><span data-stu-id="76a96-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="76a96-148">La fonction **glFeedbackBuffer** écrit également des entrées pour les bitmaps et les rectangles de pixels.</span><span class="sxs-lookup"><span data-stu-id="76a96-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="76a96-149">Des commentaires se produisent après l’élimination des polygones et l’interprétation [**glPolygonMode**](glpolygonmode.md) des polygones, de sorte que les polygones qui sont supprimés ne sont pas retournés dans la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="76a96-150">Elle peut également se produire lorsque les polygones avec plus de trois bords sont divisés en triangles, si l’implémentation OpenGL affiche des polygones en effectuant cette décomposition.</span><span class="sxs-lookup"><span data-stu-id="76a96-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="76a96-151">Vous pouvez insérer un marqueur dans la mémoire tampon de commentaires avec [**glPassThrough**](glpassthrough.md).</span><span class="sxs-lookup"><span data-stu-id="76a96-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="76a96-152">Voici la grammaire des blocs de valeurs écrites dans la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="76a96-153">Chaque primitive est indiquée avec une valeur d’identification unique suivie d’un certain nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="76a96-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="76a96-154">Les entrées de polygone incluent une valeur entière indiquant le nombre de vertex qui suivent.</span><span class="sxs-lookup"><span data-stu-id="76a96-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="76a96-155">Un vertex est renvoyé sous la forme d’un certain nombre de valeurs à virgule flottante, comme déterminé par le *type*.</span><span class="sxs-lookup"><span data-stu-id="76a96-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="76a96-156">Les couleurs sont renvoyées sous forme de quatre valeurs en mode RVBA et d’une valeur en mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="76a96-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="76a96-157">feedbackList < feedbackItem feedbackList \| feedbackItem</span><span class="sxs-lookup"><span data-stu-id="76a96-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="76a96-158">feedbackItem < point \| LineSegment \| Polygon \| bitmap \| pixelRectangle \| PassThru</span><span class="sxs-lookup"><span data-stu-id="76a96-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="76a96-159">point < sommet du jeton de \_ point GL \_</span><span class="sxs-lookup"><span data-stu-id="76a96-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="76a96-160">lineSegment < jeton de ligne GL vertex vertex de la \_ \_ \| ligne GL de \_ \_ réinitialisation du \_ jeton de sommet</span><span class="sxs-lookup"><span data-stu-id="76a96-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="76a96-161">Polygon < \_ jeton de polygone GL \_ n</span><span class="sxs-lookup"><span data-stu-id="76a96-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="76a96-162">polyspec < vertex vertex vertex vertex vertex \|</span><span class="sxs-lookup"><span data-stu-id="76a96-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="76a96-163">bitmap < vertex de jeton de \_ bitmap GL \_</span><span class="sxs-lookup"><span data-stu-id="76a96-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="76a96-164">pixelRectangle < GL-créer un vertex de jeton de pixel de \_ \_ \_ \| \_ copie GL \_ \_ de nuance de pixel</span><span class="sxs-lookup"><span data-stu-id="76a96-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="76a96-165">valeur de jeton de transmission de transfert de < du GL passThru \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="76a96-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="76a96-166">vertex < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture</span><span class="sxs-lookup"><span data-stu-id="76a96-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="76a96-167">valeur de la valeur de < 2D</span><span class="sxs-lookup"><span data-stu-id="76a96-167">2d <  value value</span></span>

<span data-ttu-id="76a96-168">valeur de la valeur de la valeur de < 3D</span><span class="sxs-lookup"><span data-stu-id="76a96-168">3d <  value value value</span></span>

<span data-ttu-id="76a96-169">3dColor < valeur de la valeur de valeur de valeur</span><span class="sxs-lookup"><span data-stu-id="76a96-169">3dColor <  value value value color</span></span>

<span data-ttu-id="76a96-170">3dColorTexture < valeur valeur valeur couleur Tex</span><span class="sxs-lookup"><span data-stu-id="76a96-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="76a96-171">4dColorTexture < valeur valeur valeur valeur couleur Tex</span><span class="sxs-lookup"><span data-stu-id="76a96-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="76a96-172">index de couleur < RVBA \|</span><span class="sxs-lookup"><span data-stu-id="76a96-172">color <  rgba \| index</span></span>

<span data-ttu-id="76a96-173">valeur de valeur de valeur de la valeur de < RVBA</span><span class="sxs-lookup"><span data-stu-id="76a96-173">rgba <  value value value value</span></span>

<span data-ttu-id="76a96-174">valeur de < d’index</span><span class="sxs-lookup"><span data-stu-id="76a96-174">index <  value</span></span>

<span data-ttu-id="76a96-175">valeur de valeur de valeur de valeur <</span><span class="sxs-lookup"><span data-stu-id="76a96-175">tex <  value value value value</span></span>

<span data-ttu-id="76a96-176">Le paramètre de *valeur* est un nombre à virgule flottante, et *n* est un entier à virgule flottante qui donne le nombre de vertex du polygone.</span><span class="sxs-lookup"><span data-stu-id="76a96-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="76a96-177">Les éléments suivants sont des constantes à virgule flottante symboliques : \_ jeton de point GL \_ , jeton de \_ ligne GL \_ , jeton de \_ \_ réinitialisation de ligne GL \_ , jeton de \_ polygone GL \_ , jeton de \_ bitmap GL, jeton de texte \_ \_ de dessin GL \_ \_ , jeton de copie GL de \_ \_ pixel \_ et jeton de transfert de GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="76a96-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="76a96-178">\_ \_ Le jeton de réinitialisation de ligne GL \_ est renvoyé chaque fois que le modèle de ligne stipple est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="76a96-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="76a96-179">Les données retournées en tant que vertex dépendent du *type* de commentaires.</span><span class="sxs-lookup"><span data-stu-id="76a96-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="76a96-180">Le tableau suivant donne la correspondance entre le *type* et le nombre de valeurs par vertex ; *k* est 1 en mode d’index de couleurs et 4 en mode RVBA.</span><span class="sxs-lookup"><span data-stu-id="76a96-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="76a96-181">Type</span><span class="sxs-lookup"><span data-stu-id="76a96-181">Type</span></span>                   | <span data-ttu-id="76a96-182">Coordinates</span><span class="sxs-lookup"><span data-stu-id="76a96-182">Coordinates</span></span>        | <span data-ttu-id="76a96-183">Couleur</span><span class="sxs-lookup"><span data-stu-id="76a96-183">Color</span></span> | <span data-ttu-id="76a96-184">Texture</span><span class="sxs-lookup"><span data-stu-id="76a96-184">Texture</span></span> | <span data-ttu-id="76a96-185">Nombre total de valeurs</span><span class="sxs-lookup"><span data-stu-id="76a96-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="76a96-186">COMPTABILITÉ \_ 2D</span><span class="sxs-lookup"><span data-stu-id="76a96-186">GL\_2D</span></span>                 | <span data-ttu-id="76a96-187">*x*, *y*</span><span class="sxs-lookup"><span data-stu-id="76a96-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="76a96-188">2</span><span class="sxs-lookup"><span data-stu-id="76a96-188">2</span></span>                      |
| <span data-ttu-id="76a96-189">\_3D GL</span><span class="sxs-lookup"><span data-stu-id="76a96-189">GL\_3D</span></span>                 | <span data-ttu-id="76a96-190">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="76a96-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="76a96-191">3</span><span class="sxs-lookup"><span data-stu-id="76a96-191">3</span></span>                      |
| <span data-ttu-id="76a96-192">\_Couleur 3D \_ GL</span><span class="sxs-lookup"><span data-stu-id="76a96-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="76a96-193">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="76a96-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="76a96-194">*k*</span><span class="sxs-lookup"><span data-stu-id="76a96-194">*k*</span></span>   |         | <span data-ttu-id="76a96-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="76a96-195">3 + *k*</span></span>                |
| <span data-ttu-id="76a96-196">\_Texture de \_ couleur \_ 3D GL</span><span class="sxs-lookup"><span data-stu-id="76a96-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="76a96-197">*x*, *y*, *z*,</span><span class="sxs-lookup"><span data-stu-id="76a96-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="76a96-198">*k*</span><span class="sxs-lookup"><span data-stu-id="76a96-198">*k*</span></span>   | <span data-ttu-id="76a96-199">4</span><span class="sxs-lookup"><span data-stu-id="76a96-199">4</span></span>       | <span data-ttu-id="76a96-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="76a96-200">7 + *k*</span></span>                |
| <span data-ttu-id="76a96-201">TEXTURE GL de \_ \_ couleur 4D \_</span><span class="sxs-lookup"><span data-stu-id="76a96-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="76a96-202">*x*, *y*, *z*, *w*</span><span class="sxs-lookup"><span data-stu-id="76a96-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="76a96-203">*k*</span><span class="sxs-lookup"><span data-stu-id="76a96-203">*k*</span></span>   | <span data-ttu-id="76a96-204">4</span><span class="sxs-lookup"><span data-stu-id="76a96-204">4</span></span>       | <span data-ttu-id="76a96-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="76a96-205">8 + *k*</span></span>                |



 

<span data-ttu-id="76a96-206">Les coordonnées des sommets de commentaires sont exprimées en coordonnées de fenêtre, sauf *w*, qui est en coordonnées de clip.</span><span class="sxs-lookup"><span data-stu-id="76a96-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="76a96-207">Les couleurs de commentaires sont claires, si l’éclairage est activé.</span><span class="sxs-lookup"><span data-stu-id="76a96-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="76a96-208">Des coordonnées de texture de commentaires sont générées si la génération de coordonnées de texture est activée.</span><span class="sxs-lookup"><span data-stu-id="76a96-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="76a96-209">Elles sont toujours transformées par la matrice de texture.</span><span class="sxs-lookup"><span data-stu-id="76a96-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="76a96-210">La fonction **glFeedbackBuffer** , lorsqu’elle est utilisée dans une liste d’affichage, n’est pas compilée dans la liste d’affichage, mais plutôt exécutée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="76a96-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="76a96-211">La fonction suivante récupère des informations relatives à **glFeedbackBuffer**:</span><span class="sxs-lookup"><span data-stu-id="76a96-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="76a96-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument GL \_ Render \_ mode</span><span class="sxs-lookup"><span data-stu-id="76a96-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="76a96-213">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76a96-213">Requirements</span></span>



| <span data-ttu-id="76a96-214">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76a96-214">Requirement</span></span> | <span data-ttu-id="76a96-215">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a96-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76a96-216">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a96-216">Minimum supported client</span></span><br/> | <span data-ttu-id="76a96-217">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a96-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="76a96-218">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a96-218">Minimum supported server</span></span><br/> | <span data-ttu-id="76a96-219">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a96-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76a96-220">En-tête</span><span class="sxs-lookup"><span data-stu-id="76a96-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="76a96-221"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="76a96-222">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="76a96-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="76a96-223"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="76a96-224">DLL</span><span class="sxs-lookup"><span data-stu-id="76a96-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76a96-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76a96-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76a96-226">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76a96-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a96-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="76a96-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="76a96-228">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="76a96-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="76a96-229">**glGet**</span><span class="sxs-lookup"><span data-stu-id="76a96-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="76a96-230">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="76a96-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="76a96-231">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="76a96-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="76a96-232">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="76a96-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="76a96-233">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="76a96-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="76a96-234">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="76a96-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





