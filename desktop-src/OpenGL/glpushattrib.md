---
title: fonction glPushAttrib (GL. h)
description: Exécute un push de la pile d’attributs.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glPushAttrib fonction OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032543"
---
# <a name="glpushattrib-function"></a><span data-ttu-id="0142a-104">glPushAttrib fonction)</span><span class="sxs-lookup"><span data-stu-id="0142a-104">glPushAttrib function</span></span>

<span data-ttu-id="0142a-105">Exécute un push de la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0142a-105">Pushes the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="0142a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0142a-106">Syntax</span></span>


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="0142a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0142a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0142a-108">*mask*</span><span class="sxs-lookup"><span data-stu-id="0142a-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="0142a-109">Masque qui indique les attributs à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="0142a-109">A mask that indicates which attributes to save.</span></span> <span data-ttu-id="0142a-110">Les constantes de masque symbolique et leur état OpenGL associé sont les suivantes (la liste des paragraphes en retrait répertorie les attributs qui sont enregistrés) :</span><span class="sxs-lookup"><span data-stu-id="0142a-110">The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):</span></span>

<dl> <dt>

<span data-ttu-id="0142a-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_bit de tampon amort \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-111"><span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL\_ACCUM\_BUFFER\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="0142a-112">Valeur effacée de la mémoire tampon d’accumulation</span><span class="sxs-lookup"><span data-stu-id="0142a-112">Accumulation buffer clear value</span></span>

</dd> <dt>

<span data-ttu-id="0142a-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit de \_ mémoire tampon de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-113"><span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL\_COLOR\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-114">\_Bit d’activation du test du GL alpha \_</span><span class="sxs-lookup"><span data-stu-id="0142a-114">GL\_ALPHA\_TEST enable bit</span></span>

<span data-ttu-id="0142a-115">Fonction de test alpha et valeur de référence</span><span class="sxs-lookup"><span data-stu-id="0142a-115">Alpha test function and reference value</span></span>

<span data-ttu-id="0142a-116">Bit d’activation de la \_ fusion GL</span><span class="sxs-lookup"><span data-stu-id="0142a-116">GL\_BLEND enable bit</span></span>

<span data-ttu-id="0142a-117">Fusion des fonctions source et de destination</span><span class="sxs-lookup"><span data-stu-id="0142a-117">Blending source and destination functions</span></span>

<span data-ttu-id="0142a-118">\_Bit d’activation du tramage GL</span><span class="sxs-lookup"><span data-stu-id="0142a-118">GL\_DITHER enable bit</span></span>

<span data-ttu-id="0142a-119">\_Paramètre de \_ mémoire tampon de dessin GL</span><span class="sxs-lookup"><span data-stu-id="0142a-119">GL\_DRAW\_BUFFER setting</span></span>

<span data-ttu-id="0142a-120">\_Bit logique d’activation du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-120">GL\_LOGIC\_OP enable bit</span></span>

<span data-ttu-id="0142a-121">Fonction Logic op</span><span class="sxs-lookup"><span data-stu-id="0142a-121">Logic op function</span></span>

<span data-ttu-id="0142a-122">Valeurs claires en mode couleur et en mode index</span><span class="sxs-lookup"><span data-stu-id="0142a-122">Color-mode and index-mode clear values</span></span>

<span data-ttu-id="0142a-123">Writemasks en mode couleur et en mode index</span><span class="sxs-lookup"><span data-stu-id="0142a-123">Color-mode and index-mode writemasks</span></span>

</dd> <dt>

<span data-ttu-id="0142a-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_bit actuel du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-124"><span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL\_CURRENT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-125">Couleur RVBA actuelle</span><span class="sxs-lookup"><span data-stu-id="0142a-125">Current RGBA color</span></span>

<span data-ttu-id="0142a-126">Index des couleurs actuelles</span><span class="sxs-lookup"><span data-stu-id="0142a-126">Current color index</span></span>

<span data-ttu-id="0142a-127">Vecteur normal actuel</span><span class="sxs-lookup"><span data-stu-id="0142a-127">Current normal vector</span></span>

<span data-ttu-id="0142a-128">Coordonnées de texture actuelles</span><span class="sxs-lookup"><span data-stu-id="0142a-128">Current texture coordinates</span></span>

<span data-ttu-id="0142a-129">Position raster actuelle indicateur de \_ la \_ position raster \_ actuelle de la position raster \_</span><span class="sxs-lookup"><span data-stu-id="0142a-129">Current raster position GL\_CURRENT\_RASTER\_POSITION\_VALID flag</span></span>

<span data-ttu-id="0142a-130">Couleur RVBA associée à la position de la trame actuelle</span><span class="sxs-lookup"><span data-stu-id="0142a-130">RGBA color associated with current raster position</span></span>

<span data-ttu-id="0142a-131">Index de couleurs associé à la position de la trame actuelle</span><span class="sxs-lookup"><span data-stu-id="0142a-131">Color index associated with current raster position</span></span>

<span data-ttu-id="0142a-132">Coordonnées de texture associées à la position de trame actuelle</span><span class="sxs-lookup"><span data-stu-id="0142a-132">Texture coordinates associated with current raster position</span></span>

<span data-ttu-id="0142a-133">Indicateur de l’indicateur de périphérie du GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-133">GL\_EDGE\_FLAG flag</span></span>

</dd> <dt>

<span data-ttu-id="0142a-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_bit de \_ mémoire tampon de profondeur GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-134"><span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL\_DEPTH\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-135">\_Bit d’activation du test de profondeur du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-135">GL\_DEPTH\_TEST enable bit</span></span>

<span data-ttu-id="0142a-136">Fonction de test de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="0142a-136">Depth buffer test function</span></span>

<span data-ttu-id="0142a-137">Valeur effacée de la mémoire tampon de profondeur</span><span class="sxs-lookup"><span data-stu-id="0142a-137">Depth buffer clear value</span></span>

<span data-ttu-id="0142a-138">Profondeur du GL \_ \_ WRITEMASK activer le bit</span><span class="sxs-lookup"><span data-stu-id="0142a-138">GL\_DEPTH\_WRITEMASK enable bit</span></span>

</dd> <dt>

<span data-ttu-id="0142a-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit d’activation du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-139"><span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL\_ENABLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-140">Indicateur de test de comptabilité \_ alpha \_</span><span class="sxs-lookup"><span data-stu-id="0142a-140">GL\_ALPHA\_TEST flag</span></span>

<span data-ttu-id="0142a-141">\_Indicateur de \_ normalisation automatique du GL</span><span class="sxs-lookup"><span data-stu-id="0142a-141">GL\_AUTO\_NORMAL flag</span></span>

<span data-ttu-id="0142a-142">Indicateur de fusion du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-142">GL\_BLEND flag</span></span>

<span data-ttu-id="0142a-143">Activer le service bits pour les plans de découpage définissables par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0142a-143">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="0142a-144">\_matériau de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-144">GL\_COLOR\_MATERIAL</span></span>

<span data-ttu-id="0142a-145">Indicateur de visage de \_ CULLING GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-145">GL\_CULL\_FACE flag</span></span>

<span data-ttu-id="0142a-146">Indicateur de test de \_ profondeur du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-146">GL\_DEPTH\_TEST flag</span></span>

<span data-ttu-id="0142a-147">\_Indicateur de tramage GL</span><span class="sxs-lookup"><span data-stu-id="0142a-147">GL\_DITHER flag</span></span>

<span data-ttu-id="0142a-148">\_Indicateur de brouillard GL</span><span class="sxs-lookup"><span data-stu-id="0142a-148">GL\_FOG flag</span></span>

<span data-ttu-id="0142a-149">GL \_ clair *i* où 0 <= *i* < des \_ lumières du GL Max \_</span><span class="sxs-lookup"><span data-stu-id="0142a-149">GL\_LIGHT *i* where 0 <= *i* < GL\_MAX\_LIGHTS</span></span>

<span data-ttu-id="0142a-150">\_Indicateur d’éclairage GL</span><span class="sxs-lookup"><span data-stu-id="0142a-150">GL\_LIGHTING flag</span></span>

<span data-ttu-id="0142a-151">Indicateur de lissage de \_ ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-151">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="0142a-152">\_ \_ Indicateur STIPPLE de la ligne GL</span><span class="sxs-lookup"><span data-stu-id="0142a-152">GL\_LINE\_STIPPLE flag</span></span>

<span data-ttu-id="0142a-153">Indicateur de logique de l' \_ op GL couleur \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-153">GL\_COLOR\_LOGIC\_OP flag</span></span>

<span data-ttu-id="0142a-154">\_Indicateur d' \_ op logique d’index GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-154">GL\_INDEX\_LOGIC\_OP flag</span></span>

<span data-ttu-id="0142a-155">GL \_ Map1 \_ x où x est un type de carte</span><span class="sxs-lookup"><span data-stu-id="0142a-155">GL\_MAP1\_x where x is a map type</span></span>

<span data-ttu-id="0142a-156">GL \_ map2 \_ x où x est un type de carte</span><span class="sxs-lookup"><span data-stu-id="0142a-156">GL\_MAP2\_x where x is a map type</span></span>

<span data-ttu-id="0142a-157">\_Indicateur de normalisation GL</span><span class="sxs-lookup"><span data-stu-id="0142a-157">GL\_NORMALIZE flag</span></span>

<span data-ttu-id="0142a-158">Indicateur de lissage du \_ point GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-158">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="0142a-159">\_Indicateur de \_ ligne de décalage du polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-159">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="0142a-160">\_Indicateur de \_ remplissage de décalage de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-160">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="0142a-161">\_Indicateur de \_ point de décalage de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-161">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="0142a-162">\_Indicateur de lissage de polygones GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-162">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="0142a-163">\_Indicateur de STIPPLE de polygones GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-163">GL\_POLYGON\_STIPPLE flag</span></span>

<span data-ttu-id="0142a-164">Indicateur de test de \_ ciseaux du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-164">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="0142a-165">Indicateur de test de \_ stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-165">GL\_STENCIL\_TEST flag</span></span>

<span data-ttu-id="0142a-166">\_ \_ Indicateur 1D de la texture GL</span><span class="sxs-lookup"><span data-stu-id="0142a-166">GL\_TEXTURE\_1D flag</span></span>

<span data-ttu-id="0142a-167">\_Indicateur de texture GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="0142a-167">GL\_TEXTURE\_2D flag</span></span>

<span data-ttu-id="0142a-168">Flags GL \_ texture \_ GEN \_ x où x est S, T, R ou Q</span><span class="sxs-lookup"><span data-stu-id="0142a-168">Flags GL\_TEXTURE\_GEN\_x where x is S, T, R, or Q</span></span>

</dd> <dt>

<span data-ttu-id="0142a-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_bit d’évaluation du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-169"><span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL\_EVAL\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-170">GL \_ Map1 \_ x active bits, où x est un type de carte</span><span class="sxs-lookup"><span data-stu-id="0142a-170">GL\_MAP1\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="0142a-171">GL \_ map2 \_ x active bits, où x est un type de carte</span><span class="sxs-lookup"><span data-stu-id="0142a-171">GL\_MAP2\_x enable bits, where x is a map type</span></span>

<span data-ttu-id="0142a-172">points de terminaison de grille 1D et divisions</span><span class="sxs-lookup"><span data-stu-id="0142a-172">1-D grid endpoints and divisions</span></span>

<span data-ttu-id="0142a-173">points de terminaison de grille 2D et divisions</span><span class="sxs-lookup"><span data-stu-id="0142a-173">2-D grid endpoints and divisions</span></span>

<span data-ttu-id="0142a-174">Bit d’activation de la \_ normalisation automatique du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-174">GL\_AUTO\_NORMAL enable bit</span></span>

</dd> <dt>

<span data-ttu-id="0142a-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-175"><span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL\_FOG\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-176">\_Indicateur d’activation du brouillard GL</span><span class="sxs-lookup"><span data-stu-id="0142a-176">GL\_FOG enable flag</span></span>

<span data-ttu-id="0142a-177">Couleur de brouillard</span><span class="sxs-lookup"><span data-stu-id="0142a-177">Fog color</span></span>

<span data-ttu-id="0142a-178">Densité de brouillard</span><span class="sxs-lookup"><span data-stu-id="0142a-178">Fog density</span></span>

<span data-ttu-id="0142a-179">Démarrage du brouillard linéaire</span><span class="sxs-lookup"><span data-stu-id="0142a-179">Linear fog start</span></span>

<span data-ttu-id="0142a-180">Fin du brouillard linéaire</span><span class="sxs-lookup"><span data-stu-id="0142a-180">Linear fog end</span></span>

<span data-ttu-id="0142a-181">Index de brouillard</span><span class="sxs-lookup"><span data-stu-id="0142a-181">Fog index</span></span>

<span data-ttu-id="0142a-182">Valeur du mode de \_ brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-182">GL\_FOG\_MODE value</span></span>

</dd> <dt>

<span data-ttu-id="0142a-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit indicateur \_ GL</span><span class="sxs-lookup"><span data-stu-id="0142a-183"><span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL\_HINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-184">Paramètre de l’indicateur de correction de la \_ perspective GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-184">GL\_PERSPECTIVE\_CORRECTION\_HINT setting</span></span>

<span data-ttu-id="0142a-185">\_Paramètre d' \_ indicateur d’arrondi de point GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-185">GL\_POINT\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="0142a-186">\_Paramètre d' \_ indicateur de lissage de ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-186">GL\_LINE\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="0142a-187">\_Paramètre d' \_ indicateur de lissage de polygones GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-187">GL\_POLYGON\_SMOOTH\_HINT setting</span></span>

<span data-ttu-id="0142a-188">Paramètre de l' \_ indicateur de brouillard GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-188">GL\_FOG\_HINT setting</span></span>

</dd> <dt>

<span data-ttu-id="0142a-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit d’éclairage GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-189"><span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL\_LIGHTING\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-190">Bit de couleur GL- \_ \_ activer le bit</span><span class="sxs-lookup"><span data-stu-id="0142a-190">GL\_COLOR\_MATERIAL enable bit</span></span>

<span data-ttu-id="0142a-191">\_Valeur de \_ face du matériau de couleur GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-191">GL\_COLOR\_MATERIAL\_FACE value</span></span>

<span data-ttu-id="0142a-192">Paramètres de matériau de couleur qui effectuent le suivi de la couleur actuelle</span><span class="sxs-lookup"><span data-stu-id="0142a-192">Color material parameters that are tracking the current color</span></span>

<span data-ttu-id="0142a-193">Couleur de scène ambiante</span><span class="sxs-lookup"><span data-stu-id="0142a-193">Ambient scene color</span></span>

<span data-ttu-id="0142a-194">\_Valeur de \_ la \_ visionneuse locale du modèle de lumière GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-194">GL\_LIGHT\_MODEL\_LOCAL\_VIEWER value</span></span>

<span data-ttu-id="0142a-195">\_Paramètre côté « GL Light \_ Model \_ deux \_ côtés »</span><span class="sxs-lookup"><span data-stu-id="0142a-195">GL\_LIGHT\_MODEL\_TWO\_SIDE setting</span></span>

<span data-ttu-id="0142a-196">Bit d’activation de l' \_ éclairage GL</span><span class="sxs-lookup"><span data-stu-id="0142a-196">GL\_LIGHTING enable bit</span></span>

<span data-ttu-id="0142a-197">Activer le bit pour chaque lumière</span><span class="sxs-lookup"><span data-stu-id="0142a-197">Enable bit for each light</span></span>

<span data-ttu-id="0142a-198">Intensité ambiante, diffuse et spéculaire pour chaque lumière</span><span class="sxs-lookup"><span data-stu-id="0142a-198">Ambient, diffuse, and specular intensity for each light</span></span>

<span data-ttu-id="0142a-199">Orientation, position, exposant et angle de coupure pour chaque lumière</span><span class="sxs-lookup"><span data-stu-id="0142a-199">Direction, position, exponent, and cutoff angle for each light</span></span>

<span data-ttu-id="0142a-200">Facteurs d’atténuation constante, linéaire et quadratique pour chaque lumière</span><span class="sxs-lookup"><span data-stu-id="0142a-200">Constant, linear, and quadratic attenuation factors for each light</span></span>

<span data-ttu-id="0142a-201">Couleur ambiante, diffuse, spéculaire et émissif pour chaque matière</span><span class="sxs-lookup"><span data-stu-id="0142a-201">Ambient, diffuse, specular, and emissive color for each material</span></span>

<span data-ttu-id="0142a-202">Index de couleurs ambiants, diffuses et spéculaires pour chaque matériau</span><span class="sxs-lookup"><span data-stu-id="0142a-202">Ambient, diffuse, and specular color indexes for each material</span></span>

<span data-ttu-id="0142a-203">Exposant spéculaire pour chaque paramètre de modèle d' \_ ombrage de la comptabilité matières \_</span><span class="sxs-lookup"><span data-stu-id="0142a-203">Specular exponent for each material GL\_SHADE\_MODEL setting</span></span>

</dd> <dt>

<span data-ttu-id="0142a-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit de ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-204"><span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL\_LINE\_BIT</span></span> 
</dt> <dd>

<span data-ttu-id="0142a-205">Indicateur de lissage de \_ ligne GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-205">GL\_LINE\_SMOOTH flag</span></span>

<span data-ttu-id="0142a-206">Bit de STIPPLE de ligne GL- \_ \_ activer</span><span class="sxs-lookup"><span data-stu-id="0142a-206">GL\_LINE\_STIPPLE enable bit</span></span>

<span data-ttu-id="0142a-207">Modèle de stipple de ligne et compteur de répétition</span><span class="sxs-lookup"><span data-stu-id="0142a-207">Line stipple pattern and repeat counter</span></span>

<span data-ttu-id="0142a-208">Largeur de ligne</span><span class="sxs-lookup"><span data-stu-id="0142a-208">Line width</span></span>

</dd> <dt>

<span data-ttu-id="0142a-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit de liste GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-209"><span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL\_LIST\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-210">Paramètre de base de la \_ liste GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-210">GL\_LIST\_BASE setting</span></span>

</dd> <dt>

<span data-ttu-id="0142a-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit du \_ mode de pixel GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-211"><span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL\_PIXEL\_MODE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-212">\_ \_ Paramètres de décalage rouge et \_ de \_ balance rouge du GL</span><span class="sxs-lookup"><span data-stu-id="0142a-212">GL\_RED\_BIAS and GL\_RED\_SCALE settings</span></span>

<span data-ttu-id="0142a-213">\_ \_ Valeurs de l’échelle vert GL et de l' \_ échelle verte GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-213">GL\_GREEN\_BIAS and GL\_GREEN\_SCALE values</span></span>

<span data-ttu-id="0142a-214">\_Décalage bleu GL \_ et \_ échelle bleue \_ GL</span><span class="sxs-lookup"><span data-stu-id="0142a-214">GL\_BLUE\_BIAS and GL\_BLUE\_SCALE</span></span>

<span data-ttu-id="0142a-215">\_Décalage alpha du GL \_ et échelle du GL \_ alpha \_</span><span class="sxs-lookup"><span data-stu-id="0142a-215">GL\_ALPHA\_BIAS and GL\_ALPHA\_SCALE</span></span>

<span data-ttu-id="0142a-216">\_ \_ Décalage de profondeur GL et \_ échelle de profondeur GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-216">GL\_DEPTH\_BIAS and GL\_DEPTH\_SCALE</span></span>

<span data-ttu-id="0142a-217">Décalage de l’index GL \_ \_ et valeurs de décalage de l' \_ index GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-217">GL\_INDEX\_OFFSET and GL\_INDEX\_SHIFT values</span></span>

<span data-ttu-id="0142a-218">\_Couleurs de la carte GL \_ et indicateurs de stencil de la \_ carte GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-218">GL\_MAP\_COLOR and GL\_MAP\_STENCIL flags</span></span>

<span data-ttu-id="0142a-219">\_Zooms GL \_ X et \_ Zoom GL \_ Y</span><span class="sxs-lookup"><span data-stu-id="0142a-219">GL\_ZOOM\_X and GL\_ZOOM\_Y factors</span></span>

<span data-ttu-id="0142a-220">Paramètre de tampon de \_ lecture GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-220">GL\_READ\_BUFFER setting</span></span>

</dd> <dt>

<span data-ttu-id="0142a-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit de point GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-221"><span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL\_POINT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-222">Indicateur de lissage du \_ point GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-222">GL\_POINT\_SMOOTH flag</span></span>

<span data-ttu-id="0142a-223">Taille du point</span><span class="sxs-lookup"><span data-stu-id="0142a-223">Point size</span></span>

</dd> <dt>

<span data-ttu-id="0142a-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-224"><span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL\_POLYGON\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-225">Bit d’activation de la face de l' \_ élimination GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-225">GL\_CULL\_FACE enable bit</span></span>

<span data-ttu-id="0142a-226">\_Valeur du \_ mode visage d’élimination du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-226">GL\_CULL\_FACE\_MODE value</span></span>

<span data-ttu-id="0142a-227">\_Indicateur de \_ face avant GL</span><span class="sxs-lookup"><span data-stu-id="0142a-227">GL\_FRONT\_FACE indicator</span></span>

<span data-ttu-id="0142a-228">\_Paramètre du \_ mode polygone GL</span><span class="sxs-lookup"><span data-stu-id="0142a-228">GL\_POLYGON\_MODE setting</span></span>

<span data-ttu-id="0142a-229">\_Indicateur de lissage de polygones GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-229">GL\_POLYGON\_SMOOTH flag</span></span>

<span data-ttu-id="0142a-230">STIPPLE de l’activation du polygone de GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-230">GL\_POLYGON\_STIPPLE enable bit</span></span>

<span data-ttu-id="0142a-231">\_Indicateur de \_ remplissage de décalage de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-231">GL\_POLYGON\_OFFSET\_FILL flag</span></span>

<span data-ttu-id="0142a-232">\_Indicateur de \_ ligne de décalage du polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-232">GL\_POLYGON\_OFFSET\_LINE flag</span></span>

<span data-ttu-id="0142a-233">\_Indicateur de \_ point de décalage de polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-233">GL\_POLYGON\_OFFSET\_POINT flag</span></span>

<span data-ttu-id="0142a-234">\_facteur de \_ décalage du polygone GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-234">GL\_POLYGON\_OFFSET\_FACTOR</span></span>

<span data-ttu-id="0142a-235">\_unités de décalage de polygones GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-235">GL\_POLYGON\_OFFSET\_UNITS</span></span>

</dd> <dt>

<span data-ttu-id="0142a-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_STIPPLE- \_ \_ bit de polygone de GL</span><span class="sxs-lookup"><span data-stu-id="0142a-236"><span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL\_POLYGON\_STIPPLE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-237">Image Polygon stipple</span><span class="sxs-lookup"><span data-stu-id="0142a-237">Polygon stipple image</span></span>

</dd> <dt>

<span data-ttu-id="0142a-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_bit de ciseaux de GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-238"><span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL\_SCISSOR\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-239">Indicateur de test de \_ ciseaux du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-239">GL\_SCISSOR\_TEST flag</span></span>

<span data-ttu-id="0142a-240">Zone de ciseaux</span><span class="sxs-lookup"><span data-stu-id="0142a-240">Scissor box</span></span>

</dd> <dt>

<span data-ttu-id="0142a-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_bit de \_ tampon de stencil du GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-241"><span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL\_STENCIL\_BUFFER\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-242">\_Bit d’activation du test du gabarit GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-242">GL\_STENCIL\_TEST enable bit</span></span>

<span data-ttu-id="0142a-243">Fonction de stencil et valeur de référence</span><span class="sxs-lookup"><span data-stu-id="0142a-243">Stencil function and reference value</span></span>

<span data-ttu-id="0142a-244">Masque de valeur de stencil</span><span class="sxs-lookup"><span data-stu-id="0142a-244">Stencil value mask</span></span>

<span data-ttu-id="0142a-245">Actions de réussite de la passe de tampon d’échec, de réussite et de profondeur du stencil</span><span class="sxs-lookup"><span data-stu-id="0142a-245">Stencil fail, pass, and depth buffer pass actions</span></span>

<span data-ttu-id="0142a-246">Valeur Clear de la mémoire tampon du stencil</span><span class="sxs-lookup"><span data-stu-id="0142a-246">Stencil buffer clear value</span></span>

<span data-ttu-id="0142a-247">Tampon de stencil writemask</span><span class="sxs-lookup"><span data-stu-id="0142a-247">Stencil buffer writemask</span></span>

</dd> <dt>

<span data-ttu-id="0142a-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit de texture GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-248"><span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL\_TEXTURE\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-249">Activer bits pour les quatre coordonnées de texture</span><span class="sxs-lookup"><span data-stu-id="0142a-249">Enable bits for the four texture coordinates</span></span>

<span data-ttu-id="0142a-250">Couleur de la bordure pour chaque image de texture</span><span class="sxs-lookup"><span data-stu-id="0142a-250">Border color for each texture image</span></span>

<span data-ttu-id="0142a-251">Fonction minimisation pour chaque image de texture</span><span class="sxs-lookup"><span data-stu-id="0142a-251">Minification function for each texture image</span></span>

<span data-ttu-id="0142a-252">Fonction d’agrandissement pour chaque image de texture</span><span class="sxs-lookup"><span data-stu-id="0142a-252">Magnification function for each texture image</span></span>

<span data-ttu-id="0142a-253">Coordonnées de texture et mode habillage pour chaque image de texture</span><span class="sxs-lookup"><span data-stu-id="0142a-253">Texture coordinates and wrap mode for each texture image</span></span>

<span data-ttu-id="0142a-254">Couleur et mode pour chaque environnement de texture</span><span class="sxs-lookup"><span data-stu-id="0142a-254">Color and mode for each texture environment</span></span>

<span data-ttu-id="0142a-255">Activer bits GL \_ texture \_ GEN \_ *x*; *x* est S, T, R et Q</span><span class="sxs-lookup"><span data-stu-id="0142a-255">Enable bits GL\_TEXTURE\_GEN\_*x*; *x* is S, T, R, and Q</span></span>

<span data-ttu-id="0142a-256">\_ \_ \_ Paramètre du mode de la génération de texture GL pour S, T, R et Q</span><span class="sxs-lookup"><span data-stu-id="0142a-256">GL\_TEXTURE\_GEN\_MODE setting for S, T, R, and Q</span></span>

<span data-ttu-id="0142a-257">équations de plan glTexGen pour S, T, R et Q</span><span class="sxs-lookup"><span data-stu-id="0142a-257">glTexGen plane equations for S, T, R, and Q</span></span>

</dd> <dt>

<span data-ttu-id="0142a-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit de transformation GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-258"><span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL\_TRANSFORM\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-259">Coefficients des six plans de découpage</span><span class="sxs-lookup"><span data-stu-id="0142a-259">Coefficients of the six clipping planes</span></span>

<span data-ttu-id="0142a-260">Activer le service bits pour les plans de découpage définissables par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="0142a-260">Enable bits for the user-definable clipping planes</span></span>

<span data-ttu-id="0142a-261">Valeur du mode de \_ matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-261">GL\_MATRIX\_MODE value</span></span>

<span data-ttu-id="0142a-262">\_Indicateur de normalisation GL</span><span class="sxs-lookup"><span data-stu-id="0142a-262">GL\_NORMALIZE flag</span></span>

</dd> <dt>

<span data-ttu-id="0142a-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit de fenêtre d’affichage GL \_</span><span class="sxs-lookup"><span data-stu-id="0142a-263"><span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL\_VIEWPORT\_BIT</span></span>
</dt> <dd>

<span data-ttu-id="0142a-264">Plage de profondeur (proche et loin)</span><span class="sxs-lookup"><span data-stu-id="0142a-264">Depth range (near and far)</span></span>

<span data-ttu-id="0142a-265">Origine de la fenêtre d’affichage et étendue</span><span class="sxs-lookup"><span data-stu-id="0142a-265">Viewport origin and extent</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0142a-266">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0142a-266">Return value</span></span>

<span data-ttu-id="0142a-267">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0142a-267">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0142a-268">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0142a-268">Error codes</span></span>

<span data-ttu-id="0142a-269">Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0142a-269">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0142a-270">Nom</span><span class="sxs-lookup"><span data-stu-id="0142a-270">Name</span></span>                                                                                                  | <span data-ttu-id="0142a-271">Signification</span><span class="sxs-lookup"><span data-stu-id="0142a-271">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0142a-272"><dt>**dépassement de capacité de la \_ pile GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0142a-272"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="0142a-273">La fonction a été appelée alors que la pile d’attributs était pleine.</span><span class="sxs-lookup"><span data-stu-id="0142a-273">The function was called while the attribute stack was full.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0142a-274"><dt>**\_opération non valide du GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0142a-274"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0142a-275">La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0142a-275">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0142a-276">Notes</span><span class="sxs-lookup"><span data-stu-id="0142a-276">Remarks</span></span>

<span data-ttu-id="0142a-277">La fonction **glPushAttrib** prend un argument, un masque qui indique les groupes de variables d’État à enregistrer sur la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0142a-277">The **glPushAttrib** function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="0142a-278">Les constantes symboliques sont utilisées pour définir des bits dans le masque.</span><span class="sxs-lookup"><span data-stu-id="0142a-278">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="0142a-279">Le paramètre Mask est généralement construit en appliquant l’opération **or** logique à plusieurs de ces constantes.</span><span class="sxs-lookup"><span data-stu-id="0142a-279">The mask parameter is typically constructed by applying the logical **OR** operation to several of these constants.</span></span> <span data-ttu-id="0142a-280">Vous pouvez utiliser le masque spécial GL \_ tous \_ les \_ bits d’attrib pour enregistrer tous les États empilables.</span><span class="sxs-lookup"><span data-stu-id="0142a-280">You can use the special mask GL\_ALL\_ATTRIB\_BITS to save all stackable states.</span></span>

<span data-ttu-id="0142a-281">La fonction [**glPopAttrib**](glpopattrib.md) restaure les valeurs des variables d’état enregistrées avec la dernière commande **glPushAttrib** .</span><span class="sxs-lookup"><span data-stu-id="0142a-281">The [**glPopAttrib**](glpopattrib.md) function restores the values of the state variables saved with the last **glPushAttrib** command.</span></span> <span data-ttu-id="0142a-282">Ceux qui ne sont pas enregistrés restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="0142a-282">Those not saved are left unchanged.</span></span>

<span data-ttu-id="0142a-283">C’est une erreur de transmettre des attributs à une pile complète, ou d’afficher des attributs sur une pile vide.</span><span class="sxs-lookup"><span data-stu-id="0142a-283">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="0142a-284">Dans les deux cas, l’indicateur d’erreur est défini et aucune autre modification n’est apportée à l’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="0142a-284">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="0142a-285">Initialement, la pile d’attributs est vide.</span><span class="sxs-lookup"><span data-stu-id="0142a-285">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="0142a-286">Toutes les valeurs de l’État OpenGL ne peuvent pas être enregistrées dans la pile d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0142a-286">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="0142a-287">Par exemple, vous ne pouvez pas enregistrer l’état du Pack de pixels et décompresser, l’état du mode de rendu et l’état de sélection et de commentaires.</span><span class="sxs-lookup"><span data-stu-id="0142a-287">For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.</span></span>

<span data-ttu-id="0142a-288">La profondeur de la pile d’attributs dépend de l’implémentation, mais elle doit être au moins égale à 16.</span><span class="sxs-lookup"><span data-stu-id="0142a-288">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="0142a-289">Les fonctions suivantes récupèrent les informations relatives à **glPushAttrib** et [**glPopAttrib**](glpopattrib.md):</span><span class="sxs-lookup"><span data-stu-id="0142a-289">The following functions retrieve information related to **glPushAttrib** and [**glPopAttrib**](glpopattrib.md):</span></span>

<span data-ttu-id="0142a-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument la \_ profondeur de la pile GL attrib \_ \_</span><span class="sxs-lookup"><span data-stu-id="0142a-290">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="0142a-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL max. profondeur de la \_ \_ \_ pile \_</span><span class="sxs-lookup"><span data-stu-id="0142a-291">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="0142a-292">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0142a-292">Requirements</span></span>



| <span data-ttu-id="0142a-293">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0142a-293">Requirement</span></span> | <span data-ttu-id="0142a-294">Valeur</span><span class="sxs-lookup"><span data-stu-id="0142a-294">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0142a-295">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0142a-295">Minimum supported client</span></span><br/> | <span data-ttu-id="0142a-296">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0142a-296">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0142a-297">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0142a-297">Minimum supported server</span></span><br/> | <span data-ttu-id="0142a-298">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0142a-298">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0142a-299">En-tête</span><span class="sxs-lookup"><span data-stu-id="0142a-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="0142a-300"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0142a-300"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0142a-301">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0142a-301">Library</span></span><br/>                  | <dl> <span data-ttu-id="0142a-302"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0142a-302"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0142a-303">DLL</span><span class="sxs-lookup"><span data-stu-id="0142a-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0142a-304"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0142a-304"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0142a-305">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0142a-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0142a-306">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0142a-306">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0142a-307">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0142a-307">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0142a-308">**glGet**</span><span class="sxs-lookup"><span data-stu-id="0142a-308">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="0142a-309">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="0142a-309">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="0142a-310">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="0142a-310">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="0142a-311">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="0142a-311">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="0142a-312">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="0142a-312">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="0142a-313">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="0142a-313">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="0142a-314">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="0142a-314">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="0142a-315">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="0142a-315">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="0142a-316">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="0142a-316">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="0142a-317">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="0142a-317">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="0142a-318">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="0142a-318">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="0142a-319">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="0142a-319">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="0142a-320">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="0142a-320">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="0142a-321">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="0142a-321">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="0142a-322">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0142a-322">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





