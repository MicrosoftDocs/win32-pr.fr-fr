---
title: C (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- ordinateurs clients
- mémoire du client
- coordonnées du clip
- découper
- index des couleurs
- mode d’index des couleurs
- cartes de couleur
- components
- contextes
- frontière
- enveloppe convexe
- système de coordonnées
- élimination
- matrice actuelle
- position du raster actuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032252"
---
# <a name="c-opengl"></a><span data-ttu-id="711a6-118">C (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="711a6-118">C (OpenGL)</span></span>

<span data-ttu-id="711a6-119">[A](a.md) [B](b.md) C [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="711a6-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="711a6-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**ordinateur client**</span><span class="sxs-lookup"><span data-stu-id="711a6-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-121">Ordinateur à partir duquel les commandes OpenGL sont émises.</span><span class="sxs-lookup"><span data-stu-id="711a6-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="711a6-122">L’ordinateur qui émet des commandes OpenGL peut être connecté via un réseau à un autre ordinateur qui exécute les commandes, ou les commandes peuvent être émises et exécutées sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="711a6-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="711a6-123">Voir aussi [serveur](s.md).</span><span class="sxs-lookup"><span data-stu-id="711a6-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="711a6-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**mémoire du client**</span><span class="sxs-lookup"><span data-stu-id="711a6-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-125">La mémoire principale (où les variables de programme sont stockées) de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="711a6-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordonnées du clip**</span><span class="sxs-lookup"><span data-stu-id="711a6-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-127">Système de coordonnées qui suit la transformation par la matrice de projection et précède la Division de perspective.</span><span class="sxs-lookup"><span data-stu-id="711a6-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="711a6-128">Vue-le découpage du volume est effectué en coordonnées de clip, mais pas le découpage propre à l’application.</span><span class="sxs-lookup"><span data-stu-id="711a6-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="711a6-129">Voir aussi [découpage propre à l’application](a.md).</span><span class="sxs-lookup"><span data-stu-id="711a6-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="711a6-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**portion**</span><span class="sxs-lookup"><span data-stu-id="711a6-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-131">Suppression de la partie d’une primitive géométrique qui est en dehors du demi-espace défini par un plan de découpage.</span><span class="sxs-lookup"><span data-stu-id="711a6-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="711a6-132">Les points sont simplement rejetés en dehors de.</span><span class="sxs-lookup"><span data-stu-id="711a6-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="711a6-133">La partie d’une ligne ou d’un polygone qui est en dehors du demi-espace est éliminée, et des vertex supplémentaires sont générés si nécessaire pour terminer la primitive dans le demi-espace de découpage.</span><span class="sxs-lookup"><span data-stu-id="711a6-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="711a6-134">Les primitives géométriques et la position raster actuelle (lorsqu’elles sont spécifiées) sont toujours coupées par rapport aux six demi-espaces définis par les plans gauche, droit, inférieur, supérieur, proche et Far du volume de la vue.</span><span class="sxs-lookup"><span data-stu-id="711a6-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="711a6-135">Les applications peuvent spécifier des plans de découpage spécifiques à l’application facultatifs à appliquer dans les coordonnées oculaires.</span><span class="sxs-lookup"><span data-stu-id="711a6-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**index des couleurs**</span><span class="sxs-lookup"><span data-stu-id="711a6-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-137">Valeur unique qui représente une couleur par nom, plutôt que par valeur.</span><span class="sxs-lookup"><span data-stu-id="711a6-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="711a6-138">Les index de couleurs OpenGL sont traités comme des valeurs continues (par exemple, des nombres à virgule flottante), tandis que des opérations telles que l’interpolation et le tramage sont effectuées sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="711a6-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="711a6-139">Toutefois, les index de couleurs stockés dans la mémoire tampon de trame sont toujours des valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="711a6-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="711a6-140">Les index à virgule flottante sont convertis en entiers en arrondissant à la valeur entière la plus proche.</span><span class="sxs-lookup"><span data-stu-id="711a6-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**mode d’index des couleurs**</span><span class="sxs-lookup"><span data-stu-id="711a6-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-142">Mode d’un contexte OpenGL dans lequel ses mémoires tampons de couleur stockent les index de couleur, plutôt que les composants de couleur rouge, vert, bleu et alpha.</span><span class="sxs-lookup"><span data-stu-id="711a6-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**carte des couleurs**</span><span class="sxs-lookup"><span data-stu-id="711a6-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-144">Tableau de mappages index-à-RGB accessibles par le matériel d’affichage.</span><span class="sxs-lookup"><span data-stu-id="711a6-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="711a6-145">Chaque index de couleur est lu à partir de la mémoire tampon de couleur, converti en une triple RVB par recherche dans la carte des couleurs, puis envoyé à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="711a6-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**-**</span><span class="sxs-lookup"><span data-stu-id="711a6-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-147">Valeur unique, continue (par exemple, à virgule flottante) qui représente une intensité ou une quantité.</span><span class="sxs-lookup"><span data-stu-id="711a6-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="711a6-148">En règle générale, une valeur de composant égale à zéro représente la valeur ou l’intensité minimale, et une valeur de composant égale à 1 représente la valeur ou l’intensité maximale, même si d’autres normalisations sont parfois utilisées.</span><span class="sxs-lookup"><span data-stu-id="711a6-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="711a6-149">Étant donné que les valeurs des composants sont interprétées dans une plage normalisée, elles sont spécifiées indépendamment de la résolution réelle.</span><span class="sxs-lookup"><span data-stu-id="711a6-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="711a6-150">Par exemple, le triple RVB (1, 1, 1) est blanc, que les tampons de couleur stockent 4, 8 ou 12 bits chacun.</span><span class="sxs-lookup"><span data-stu-id="711a6-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="711a6-151">Les composants hors limites sont généralement ancrés à la plage normalisée, non tronqués ou interprétés autrement.</span><span class="sxs-lookup"><span data-stu-id="711a6-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="711a6-152">Par exemple, la triple RGB (1,4, 1,5, 0,9) est ancrée (1,0, 1,0, 0,9) avant d’être utilisée pour mettre à jour la mémoire tampon de couleur.</span><span class="sxs-lookup"><span data-stu-id="711a6-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="711a6-153">Les niveaux rouge, vert, bleu, alpha et profondeur sont toujours traités en tant que composants, jamais en tant qu’index.</span><span class="sxs-lookup"><span data-stu-id="711a6-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**contexte**</span><span class="sxs-lookup"><span data-stu-id="711a6-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-155">Ensemble complet de variables d’État OpenGL.</span><span class="sxs-lookup"><span data-stu-id="711a6-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="711a6-156">Notez que le contenu de trame ne fait pas partie de l’État OpenGL, mais que la configuration du trame est.</span><span class="sxs-lookup"><span data-stu-id="711a6-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**frontière**</span><span class="sxs-lookup"><span data-stu-id="711a6-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-158">Condition d’un polygone dans laquelle aucune ligne droite dans le plan du polygone ne croise le polygone plus de deux fois.</span><span class="sxs-lookup"><span data-stu-id="711a6-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**forme convexe**</span><span class="sxs-lookup"><span data-stu-id="711a6-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-160">Plus petite région convexe englobant un groupe de points spécifié.</span><span class="sxs-lookup"><span data-stu-id="711a6-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="711a6-161">Dans deux dimensions, la forme convexe est trouvée d’un point de vue conceptuel en étirant une bande caoutchoutée autour des points afin que tous les points se trouvent dans la bande.</span><span class="sxs-lookup"><span data-stu-id="711a6-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**système de coordonnées**</span><span class="sxs-lookup"><span data-stu-id="711a6-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-163">Dans un espace en n dimensions, ensemble de n vecteurs linéairement indépendants ancrés à un point (appelé « origine »).</span><span class="sxs-lookup"><span data-stu-id="711a6-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="711a6-164">Un groupe de coordonnées spécifie un point dans l’espace n-dimensionnel, un ensemble de n vecteurs linéairement indépendants ancrés à un point (appelé « origine »).</span><span class="sxs-lookup"><span data-stu-id="711a6-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="711a6-165">Un groupe de coordonnées spécifie un point dans l'espace (ou un vecteur partant de l'origine) en indiquant la distance à parcourir le long de chaque vectoriel pour atteindre le point (ou pointe du vecteur).</span><span class="sxs-lookup"><span data-stu-id="711a6-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="711a6-166">(ou un vecteur à partir de l’origine) en indiquant la distance de déplacement le long de chaque vecteur pour atteindre le point (ou l’extrémité du vecteur).</span><span class="sxs-lookup"><span data-stu-id="711a6-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="711a6-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**élimination**</span><span class="sxs-lookup"><span data-stu-id="711a6-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-168">Processus d’élimination d’une facette ou d’un arrière-plan d’un polygone afin que la face ne soit pas dessinée.</span><span class="sxs-lookup"><span data-stu-id="711a6-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matrice actuelle**</span><span class="sxs-lookup"><span data-stu-id="711a6-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-170">Matrice qui transforme les coordonnées d’un système de coordonnées en coordonnées d’un autre système.</span><span class="sxs-lookup"><span data-stu-id="711a6-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="711a6-171">OpenGL contient trois matrices actuelles : la matrice modelview, qui transforme les coordonnées des objets (coordonnées spécifiées par le programmeur) en coordonnées oculaires ; la matrice de perspective, qui transforme les coordonnées oculaire en coordonnées de clip ; et la matrice de texture, qui transforme les coordonnées de texture spécifiées ou générées comme décrit par la matrice.</span><span class="sxs-lookup"><span data-stu-id="711a6-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="711a6-172">Chaque matrice actuelle est le premier élément d’une pile de matrices.</span><span class="sxs-lookup"><span data-stu-id="711a6-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="711a6-173">Chacune des trois piles peut être manipulée avec les commandes de manipulation de matrice OpenGL.</span><span class="sxs-lookup"><span data-stu-id="711a6-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="711a6-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**position du raster actuel**</span><span class="sxs-lookup"><span data-stu-id="711a6-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="711a6-175">Position de la coordonnée de la fenêtre qui spécifie le positionnement d’une primitive d’image lorsqu’elle est pixellisée.</span><span class="sxs-lookup"><span data-stu-id="711a6-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="711a6-176">La position actuelle du raster, ainsi que les autres paramètres de trame actuels, sont mis à jour lorsque glRasterpos est appelé.</span><span class="sxs-lookup"><span data-stu-id="711a6-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 




