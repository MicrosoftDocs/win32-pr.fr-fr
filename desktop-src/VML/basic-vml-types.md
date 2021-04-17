---
title: Types VML de base
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Migrez les pages Web et les applications qui reposent sur VML sur SVG ou sur d’autres normes largement prises en charge.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Langage VML (VML), types de base
- VML (langage VML), types de base
- graphiques vectoriels, types VML de base
- Langage VML (VML), types
- VML (langage VML), types
- graphiques vectoriels, types VML
- types VML de base
- type booléen
- type de fraction
- type ordonné
- type de longueur
- type de mesure
- type d’angle
- type de couleur
- type de police
- type de bitmap
- Type vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104559166"
---
# <a name="basic-vml-types"></a><span data-ttu-id="6349a-121">Types VML de base</span><span class="sxs-lookup"><span data-stu-id="6349a-121">Basic VML Types</span></span>

<span data-ttu-id="6349a-122">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6349a-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6349a-123">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6349a-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6349a-124">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="6349a-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6349a-125">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="6349a-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6349a-126">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6349a-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6349a-127">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6349a-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6349a-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="6349a-128">**Contents**</span></span>

-   [<span data-ttu-id="6349a-129">Introduction</span><span class="sxs-lookup"><span data-stu-id="6349a-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="6349a-130">boolean</span><span class="sxs-lookup"><span data-stu-id="6349a-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="6349a-131">fraction</span><span class="sxs-lookup"><span data-stu-id="6349a-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="6349a-132">ordonnée</span><span class="sxs-lookup"><span data-stu-id="6349a-132">ordinate</span></span>](#ordinate)
-   [<span data-ttu-id="6349a-133">length</span><span class="sxs-lookup"><span data-stu-id="6349a-133">length</span></span>](#length)
    -   [<span data-ttu-id="6349a-134">Autres représentations</span><span class="sxs-lookup"><span data-stu-id="6349a-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="6349a-135">unité</span><span class="sxs-lookup"><span data-stu-id="6349a-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="6349a-136">Autres représentations</span><span class="sxs-lookup"><span data-stu-id="6349a-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="6349a-137">angle</span><span class="sxs-lookup"><span data-stu-id="6349a-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="6349a-138">Autres représentations</span><span class="sxs-lookup"><span data-stu-id="6349a-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="6349a-139">color</span><span class="sxs-lookup"><span data-stu-id="6349a-139">color</span></span>](#color)
    -   [<span data-ttu-id="6349a-140">Unités de couleur</span><span class="sxs-lookup"><span data-stu-id="6349a-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="6349a-141">Couleurs HTML</span><span class="sxs-lookup"><span data-stu-id="6349a-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="6349a-142">Couleurs du schéma</span><span class="sxs-lookup"><span data-stu-id="6349a-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="6349a-143">Couleurs système</span><span class="sxs-lookup"><span data-stu-id="6349a-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="6349a-144">Couleurs pures</span><span class="sxs-lookup"><span data-stu-id="6349a-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="6349a-145">Réglages des couleurs</span><span class="sxs-lookup"><span data-stu-id="6349a-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="6349a-146">son</span><span class="sxs-lookup"><span data-stu-id="6349a-146">font</span></span>](#font)
-   [<span data-ttu-id="6349a-147">bitmap</span><span class="sxs-lookup"><span data-stu-id="6349a-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="6349a-148">Formats de fichiers image</span><span class="sxs-lookup"><span data-stu-id="6349a-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="6349a-149">graphiques</span><span class="sxs-lookup"><span data-stu-id="6349a-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="6349a-150">Introduction</span><span class="sxs-lookup"><span data-stu-id="6349a-150">Introduction</span></span>

<span data-ttu-id="6349a-151">Cette proposition utilise un petit nombre de types de base, listés dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6349a-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="6349a-152">Type</span><span class="sxs-lookup"><span data-stu-id="6349a-152">Type</span></span>                  | <span data-ttu-id="6349a-153">Élément</span><span class="sxs-lookup"><span data-stu-id="6349a-153">Element</span></span>           | <span data-ttu-id="6349a-154">Représentation fondamentale</span><span class="sxs-lookup"><span data-stu-id="6349a-154">Fundamental Representation</span></span> | <span data-ttu-id="6349a-155">Description</span><span class="sxs-lookup"><span data-stu-id="6349a-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6349a-156">boolean</span><span class="sxs-lookup"><span data-stu-id="6349a-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="6349a-157">1 bit</span><span class="sxs-lookup"><span data-stu-id="6349a-157">1 bit</span></span>                      | <span data-ttu-id="6349a-158">Valeur booléenne : true ou false.</span><span class="sxs-lookup"><span data-stu-id="6349a-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="6349a-159">fraction</span><span class="sxs-lookup"><span data-stu-id="6349a-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="6349a-160">Numéro 2 6</span><span class="sxs-lookup"><span data-stu-id="6349a-160">number 2 6</span></span>                 | <span data-ttu-id="6349a-161">Valeur numérique, mise à l’échelle par 2 6 (65536) et stockée en tant qu’entier signé.</span><span class="sxs-lookup"><span data-stu-id="6349a-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="6349a-162">ordonnée</span><span class="sxs-lookup"><span data-stu-id="6349a-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="6349a-163">signe plus (+) de 30 bits</span><span class="sxs-lookup"><span data-stu-id="6349a-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="6349a-164">Une partie d’une coordonnée (par exemple, dans un chemin d’accès), les valeurs définies par Coord.</span><span class="sxs-lookup"><span data-stu-id="6349a-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| [<span data-ttu-id="6349a-165">length</span><span class="sxs-lookup"><span data-stu-id="6349a-165">length</span></span>](#length)     |                   | [<span data-ttu-id="6349a-166">UME</span><span class="sxs-lookup"><span data-stu-id="6349a-166">EMU</span></span>](#length)             | <span data-ttu-id="6349a-167">Longueur physique, telle que la largeur d’une ligne ou la taille d’une police.</span><span class="sxs-lookup"><span data-stu-id="6349a-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="6349a-168">unité</span><span class="sxs-lookup"><span data-stu-id="6349a-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="6349a-169">UME ou numéro 2 6</span><span class="sxs-lookup"><span data-stu-id="6349a-169">EMU or number 2 6</span></span>          | <span data-ttu-id="6349a-170">Soit une longueur physique, notamment un nombre de pixels de l’appareil, soit une fraction d’une autre quantité.</span><span class="sxs-lookup"><span data-stu-id="6349a-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="6349a-171">angle</span><span class="sxs-lookup"><span data-stu-id="6349a-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="6349a-172">degrés 2 6</span><span class="sxs-lookup"><span data-stu-id="6349a-172">degrees 2 6</span></span>                | <span data-ttu-id="6349a-173">Angle ; positif dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="6349a-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="6349a-174">color</span><span class="sxs-lookup"><span data-stu-id="6349a-174">color</span></span>](#color)       | [<span data-ttu-id="6349a-175">c</span><span class="sxs-lookup"><span data-stu-id="6349a-175">c</span></span>](#color)       | <span data-ttu-id="6349a-176">complex</span><span class="sxs-lookup"><span data-stu-id="6349a-176">complex</span></span>                    | <span data-ttu-id="6349a-177">Élément qui autorise la dérivation d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="6349a-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="6349a-178">son</span><span class="sxs-lookup"><span data-stu-id="6349a-178">font</span></span>](#font)         | [<span data-ttu-id="6349a-179">son</span><span class="sxs-lookup"><span data-stu-id="6349a-179">font</span></span>](#font)     | <span data-ttu-id="6349a-180">complex</span><span class="sxs-lookup"><span data-stu-id="6349a-180">complex</span></span>                    | <span data-ttu-id="6349a-181">Description d’une police.</span><span class="sxs-lookup"><span data-stu-id="6349a-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="6349a-182">bitmap</span><span class="sxs-lookup"><span data-stu-id="6349a-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="6349a-183">bitmap</span><span class="sxs-lookup"><span data-stu-id="6349a-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="6349a-184">href</span><span class="sxs-lookup"><span data-stu-id="6349a-184">href</span></span>                       | <span data-ttu-id="6349a-185">Référence à un fichier image externe.</span><span class="sxs-lookup"><span data-stu-id="6349a-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="6349a-186">graphiques</span><span class="sxs-lookup"><span data-stu-id="6349a-186">vector</span></span>](#vector)     | [<span data-ttu-id="6349a-187">v</span><span class="sxs-lookup"><span data-stu-id="6349a-187">v</span></span>](#vector)      | <span data-ttu-id="6349a-188">complex</span><span class="sxs-lookup"><span data-stu-id="6349a-188">complex</span></span>                    | <span data-ttu-id="6349a-189">Description d’un tracé de vecteur</span><span class="sxs-lookup"><span data-stu-id="6349a-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="6349a-190">La « représentation fondamentale » est la représentation de précision la plus élevée que la proposition requiert une implémentation conforme pour tenir à jour ; les données seront perdues si l’implémentation n’est pas en mesure de représenter les données dans la précision requise.</span><span class="sxs-lookup"><span data-stu-id="6349a-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="6349a-191">Les types de couleur, de police et de vecteur correspondent à des éléments qui ont eux-mêmes une structure, ce qui n’est pas le type de base ; Toutefois, il est pratique de les traiter en tant que tels dans le cadre de cette proposition.</span><span class="sxs-lookup"><span data-stu-id="6349a-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="6349a-192">Chaque type de base non complexe a un élément associé du même nom.</span><span class="sxs-lookup"><span data-stu-id="6349a-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="6349a-193">Ces noms d’éléments sont réservés et ne peuvent pas être utilisés à d’autres fins dans les extensions, même si l’utilisation se trouve dans un élément d’extension OnView = "Skip".</span><span class="sxs-lookup"><span data-stu-id="6349a-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="6349a-194">Pour cette raison, il est possible pour une implémentation qui rencontre des données XML inconnues de fournir un stockage interne efficace du code XML inconnu tant que les valeurs sont placées dans les éléments « type ».</span><span class="sxs-lookup"><span data-stu-id="6349a-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="6349a-195">Dans le premier exemple ci-dessus, la chaîne « 1,578 » doit être stockée sous la forme d’une séquence de caractères (l’implémentation ne sait pas s’il s’agit d’une chaîne ou d’un nombre); dans le deuxième exemple, l’élément fraction indique que le contenu est un nombre, il peut donc être converti en représentation de fraction haute précision.</span><span class="sxs-lookup"><span data-stu-id="6349a-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="6349a-196">Les types complexes (y compris les bitmaps) ont des noms d’éléments associés qui sont utilisés pour délimiter la valeur.</span><span class="sxs-lookup"><span data-stu-id="6349a-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="6349a-197">Cela simplifie l’analyse en s’assurant que les tâches d’analyse plus complexes sont associées à des balises d’éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="6349a-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="6349a-198">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="6349a-199">boolean</span><span class="sxs-lookup"><span data-stu-id="6349a-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="6349a-200">Une valeur booléenne est représentée sous la forme d’un mot clé qui indique l’état de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="6349a-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="6349a-201">Les mots clés suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="6349a-201">The following keywords are defined.</span></span>



| <span data-ttu-id="6349a-202">Valeur pour true</span><span class="sxs-lookup"><span data-stu-id="6349a-202">Value for true</span></span> | <span data-ttu-id="6349a-203">Valeur pour false</span><span class="sxs-lookup"><span data-stu-id="6349a-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="6349a-204">true</span><span class="sxs-lookup"><span data-stu-id="6349a-204">true</span></span>           | <span data-ttu-id="6349a-205">false</span><span class="sxs-lookup"><span data-stu-id="6349a-205">false</span></span>           |
| <span data-ttu-id="6349a-206">Oui</span><span class="sxs-lookup"><span data-stu-id="6349a-206">yes</span></span>            | <span data-ttu-id="6349a-207">non</span><span class="sxs-lookup"><span data-stu-id="6349a-207">no</span></span>              |
| <span data-ttu-id="6349a-208">sur</span><span class="sxs-lookup"><span data-stu-id="6349a-208">on</span></span>             | <span data-ttu-id="6349a-209">arrêt</span><span class="sxs-lookup"><span data-stu-id="6349a-209">off</span></span>             |
| <span data-ttu-id="6349a-210">t</span><span class="sxs-lookup"><span data-stu-id="6349a-210">t</span></span>              | <span data-ttu-id="6349a-211">f</span><span class="sxs-lookup"><span data-stu-id="6349a-211">f</span></span>               |
| <span data-ttu-id="6349a-212">1</span><span class="sxs-lookup"><span data-stu-id="6349a-212">1</span></span>              | <span data-ttu-id="6349a-213">0</span><span class="sxs-lookup"><span data-stu-id="6349a-213">0</span></span>               |



 

<span data-ttu-id="6349a-214">Une implémentation peut écrire n’importe quelle valeur et doit reconnaître toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6349a-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="6349a-215">Une implémentation est libre de modifier les valeurs d’une représentation à une autre.</span><span class="sxs-lookup"><span data-stu-id="6349a-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="6349a-216">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="6349a-217">fraction</span><span class="sxs-lookup"><span data-stu-id="6349a-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="6349a-218">Toutes les valeurs numériques (c’est-à-dire, les valeurs de quantités sans dimension) de cette proposition peuvent être stockées sous forme d’entiers en les mettant à l’échelle de 2 6 (65536).</span><span class="sxs-lookup"><span data-stu-id="6349a-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="6349a-219">Un nombre peut être donné dans ce formulaire, avec le suffixe f ou en tant que nombre décimal sans suffixe.</span><span class="sxs-lookup"><span data-stu-id="6349a-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="6349a-220">Ainsi, les éléments hypothétiques suivants représentent la même valeur.</span><span class="sxs-lookup"><span data-stu-id="6349a-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="6349a-221">Une quantité avec le suffixe f doit être un nombre entier ; les nombres fractionnaires ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="6349a-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="6349a-222">L’entier résultant doit être représenté comme un nombre signé de complément 32 bits 2. par conséquent, la plage effective de la représentation est 32768 (en fait, inférieure à 32768 et supérieure ou égale à-32768).</span><span class="sxs-lookup"><span data-stu-id="6349a-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="6349a-223">Une implémentation conforme est requise pour conserver les valeurs exprimées sous forme de valeurs f.</span><span class="sxs-lookup"><span data-stu-id="6349a-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="6349a-224">Les valeurs représentées sous forme de nombres décimaux peuvent être converties en une valeur f et stockées de cette façon.</span><span class="sxs-lookup"><span data-stu-id="6349a-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="6349a-225">Une application est autorisée à enregistrer des valeurs générées en interne dans toute unité appropriée ; Toutefois, une valeur lue à partir d’un document existant doit être maintenue à la précision d’origine complète ou doit être convertie en valeur f.</span><span class="sxs-lookup"><span data-stu-id="6349a-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="6349a-226">Si l’implémentation ne parvient pas à effectuer cette opération, il doit avertir l’utilisateur que des données peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="6349a-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="6349a-227">(Il est possible d’émettre un tel avertissement une fois lorsque des données générées en externe sont rencontrées pour la première fois.)</span><span class="sxs-lookup"><span data-stu-id="6349a-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="6349a-228">Quand une valeur décimale est convertie au format f, l’implémentation peut utiliser n’importe quel mode d’arrondi arithmétique ; Toutefois, un nombre entier doit être converti au format f exactement.</span><span class="sxs-lookup"><span data-stu-id="6349a-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="6349a-229">Il est recommandé que les implémentations soient converties par un arrondi à moins l’infini et que la conversion soit toujours exacte.</span><span class="sxs-lookup"><span data-stu-id="6349a-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="6349a-230">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="6349a-231">ordonnée</span><span class="sxs-lookup"><span data-stu-id="6349a-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="6349a-232">Les unités du système de coordonnées établi par le repère sont d’un type nominal, appelé ordonnée.</span><span class="sxs-lookup"><span data-stu-id="6349a-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="6349a-233">Il s’agit d’une mesure de longueur, mais elle est utilisée uniquement par rapport au rectangle établi par Coord.</span><span class="sxs-lookup"><span data-stu-id="6349a-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="6349a-234">Toute valeur de type ordonné est mise à l’échelle en fonction des valeurs *w* et *h* du repère et du rapport résultant utilisé pour établir une mesure réelle sur le périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="6349a-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="6349a-235">Une implémentation conforme doit pouvoir gérer des valeurs ordonnées allant jusqu’à 30 bits plus le signe (c’est-à-dire un entier signé de 31 bits, et non un entier signé 32 bits).</span><span class="sxs-lookup"><span data-stu-id="6349a-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="6349a-236">Toutefois, il est recommandé que les implémentations tentent de produire des coordonnées pour le chemin d’accès et des éléments similaires qui ont environ 16 bits de précision.</span><span class="sxs-lookup"><span data-stu-id="6349a-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="6349a-237">Cela réduira le risque de dépassement de capacité négatif ou de dépassement de capacité dans une implémentation non conforme.</span><span class="sxs-lookup"><span data-stu-id="6349a-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="6349a-238">les valeurs ordonnées sont toujours intégrales.</span><span class="sxs-lookup"><span data-stu-id="6349a-238">ordinate values are always integral.</span></span> <span data-ttu-id="6349a-239">Une virgule décimale ne peut pas apparaître dans une valeur de type ordonnée.</span><span class="sxs-lookup"><span data-stu-id="6349a-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="6349a-240">Aucun spécificateur d’unité ne peut être ajouté aux valeurs de type ordonnée.</span><span class="sxs-lookup"><span data-stu-id="6349a-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="6349a-241">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="6349a-242">length</span><span class="sxs-lookup"><span data-stu-id="6349a-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="6349a-243">Une longueur est une mesure du monde réel ou, parfois, une mesure en pixels de périphérique.</span><span class="sxs-lookup"><span data-stu-id="6349a-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="6349a-244">Il est recommandé que les implémentations évitent l’utilisation de pixels de périphérique (PX).</span><span class="sxs-lookup"><span data-stu-id="6349a-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="6349a-245">Tous les qualificateurs d’unités [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) standard sont autorisés sur une longueur.</span><span class="sxs-lookup"><span data-stu-id="6349a-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="6349a-246">En outre, le qualificateur u.m.e. peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="6349a-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="6349a-247">Ce qualificateur fait référence à une unité (l’unité de mesure anglaise), qui est un dénominateur commun des quantités de mesure dans un usage répandu dans les graphiques informatiques.</span><span class="sxs-lookup"><span data-stu-id="6349a-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="6349a-248">L’UEM est de <sup>pouce</sup> /914400, c’est-à-dire qu’il y a 914400 UME par pouce.</span><span class="sxs-lookup"><span data-stu-id="6349a-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="6349a-249">Le tableau suivant répertorie le nombre d’Emu dans un petit nombre d’unités couramment rencontrées.</span><span class="sxs-lookup"><span data-stu-id="6349a-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="6349a-250">Nombre d’EMU</span><span class="sxs-lookup"><span data-stu-id="6349a-250">Number of EMUs</span></span> | <span data-ttu-id="6349a-251">Nombre par pouce</span><span class="sxs-lookup"><span data-stu-id="6349a-251">Number per Inch</span></span> | <span data-ttu-id="6349a-252">Nombre par millimètre</span><span class="sxs-lookup"><span data-stu-id="6349a-252">Number per Millimeter</span></span> | <span data-ttu-id="6349a-253">Description</span><span class="sxs-lookup"><span data-stu-id="6349a-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="6349a-254">360</span><span class="sxs-lookup"><span data-stu-id="6349a-254">360</span></span>            |                 | <span data-ttu-id="6349a-255">0,01</span><span class="sxs-lookup"><span data-stu-id="6349a-255">0.01</span></span>                  | <span data-ttu-id="6349a-256">HIMETRIC Win32</span><span class="sxs-lookup"><span data-stu-id="6349a-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="6349a-257">12700</span><span class="sxs-lookup"><span data-stu-id="6349a-257">12700</span></span>          | <span data-ttu-id="6349a-258">72</span><span class="sxs-lookup"><span data-stu-id="6349a-258">72</span></span>              |                       | <span data-ttu-id="6349a-259">point</span><span class="sxs-lookup"><span data-stu-id="6349a-259">"point"</span></span>                 |
| <span data-ttu-id="6349a-260">635</span><span class="sxs-lookup"><span data-stu-id="6349a-260">635</span></span>            | <span data-ttu-id="6349a-261">1440</span><span class="sxs-lookup"><span data-stu-id="6349a-261">1440</span></span>            |                       | <span data-ttu-id="6349a-262">TWIP Win32</span><span class="sxs-lookup"><span data-stu-id="6349a-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="6349a-263">762</span><span class="sxs-lookup"><span data-stu-id="6349a-263">762</span></span>            | <span data-ttu-id="6349a-264">1200</span><span class="sxs-lookup"><span data-stu-id="6349a-264">1200</span></span>            |                       | <span data-ttu-id="6349a-265">Imprimante haute résolution</span><span class="sxs-lookup"><span data-stu-id="6349a-265">High-resolution printer</span></span> |



 

<span data-ttu-id="6349a-266">Les nombres fractionnaires de EMU ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="6349a-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="6349a-267">Toute mesure doit être représentée en tant que nombre entier signé 32 bits d’EMU, ce qui limite l’amplitude d’une mesure à 2348 pouces environ 59 mètres ou 65 mètres.</span><span class="sxs-lookup"><span data-stu-id="6349a-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="6349a-268">Étant donné que les mesures font toujours référence à la taille d’un rendu sur un appareil de sortie à écran ou page nominal, elles se trouvent toujours dans cette plage.</span><span class="sxs-lookup"><span data-stu-id="6349a-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="6349a-269">Notez, toutefois, que la représentation n’est pas appropriée pour les mesures du monde réel et que, lorsque celles-ci sont enregistrées (par exemple, pour enregistrer la taille réelle d’un chemin d’accès), une autre représentation doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6349a-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="6349a-270">Une implémentation conforme est requise pour conserver les valeurs qui sont des nombres exacts de EMU.</span><span class="sxs-lookup"><span data-stu-id="6349a-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="6349a-271">Les valeurs représentées d’une autre manière peuvent être converties en une valeur UME et stockées de cette façon.</span><span class="sxs-lookup"><span data-stu-id="6349a-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="6349a-272">Une application est autorisée à enregistrer des valeurs générées en interne dans toute unité appropriée ; Toutefois, une valeur lue à partir d’un document existant doit être maintenue à la précision d’origine complète ou être convertie en valeur UME.</span><span class="sxs-lookup"><span data-stu-id="6349a-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="6349a-273">Si l’implémentation ne parvient pas à effectuer cette opération, il doit avertir l’utilisateur que des données peuvent être perdues.</span><span class="sxs-lookup"><span data-stu-id="6349a-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="6349a-274">(Il est possible d’émettre un tel avertissement une fois lorsque des données générées en externe sont rencontrées pour la première fois.)</span><span class="sxs-lookup"><span data-stu-id="6349a-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="6349a-275">Dans la pratique, les longueurs physiques sont utilisées pour des mesures relativement peu nombreuses dans cette proposition.</span><span class="sxs-lookup"><span data-stu-id="6349a-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="6349a-276">Les données les plus importantes sont généralement les données de chemin d’accès et sont encodées dans le système de coordonnées défini, en fonction de la forme, par repère.</span><span class="sxs-lookup"><span data-stu-id="6349a-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="6349a-277">Autres représentations</span><span class="sxs-lookup"><span data-stu-id="6349a-277">Alternative representations</span></span>

<span data-ttu-id="6349a-278">Les représentations de longueur standard du code HTML sont définies par [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="6349a-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="6349a-279">Les unités relatives, à l’exception du pixel, ne sont pas significatives dans le contexte dans lequel les longueurs sont utilisées dans cette proposition et ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="6349a-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="6349a-280">Si le document enregistre la taille de pixel prévue (cible), cela définit la translation des pixels en EMU ; dans le cas contraire, la valeur par défaut de 90 dpi définie par [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6349a-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="6349a-281">À l’exception de l’UEM, toute valeur peut être fournie sous la forme d’une fraction décimale.</span><span class="sxs-lookup"><span data-stu-id="6349a-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="6349a-282">Quand une valeur décimale est convertie en EMU, l’implémentation peut utiliser n’importe quel mode d’arrondi arithmétique.</span><span class="sxs-lookup"><span data-stu-id="6349a-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="6349a-283">(Le seul moyen pour une application de création de garantir un résultat particulier est de la spécifier en UME.)</span><span class="sxs-lookup"><span data-stu-id="6349a-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="6349a-284">Si aucun spécificateur d’unité n’est fourni dans une valeur de longueur, l’implémentation doit supposer l’UEM.</span><span class="sxs-lookup"><span data-stu-id="6349a-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="6349a-285">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="6349a-286">mesure</span><span class="sxs-lookup"><span data-stu-id="6349a-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="6349a-287">Une mesure est une quantité qui peut être une [longueur](#length) ou une [fraction](#fraction).</span><span class="sxs-lookup"><span data-stu-id="6349a-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="6349a-288">Cela ressemble de près aux mesures de longueur HTML et CSS, qui peuvent, dans de nombreux cas, être des mesures physiques ou des pourcentages d’une autre quantité.</span><span class="sxs-lookup"><span data-stu-id="6349a-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="6349a-289">Si aucun spécificateur d’unité n’est spécifié, la valeur doit être considérée comme une fraction décimale (ce comportement est donc hérité de la fraction, pas de la longueur).</span><span class="sxs-lookup"><span data-stu-id="6349a-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="6349a-290">Contrairement à la longueur, une valeur de pixel a une signification définie par le contexte, donc la conversion en EMU est normalement inappropriée.</span><span class="sxs-lookup"><span data-stu-id="6349a-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="6349a-291">Il existe trois représentations fondamentales possibles que l’implémentation doit gérer (c’est-à-dire qu’une représentation ne peut pas être convertie en une autre sans perte d’informations).</span><span class="sxs-lookup"><span data-stu-id="6349a-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="6349a-292">Une valeur fractionnaire doit être conservée au format [fraction](#fraction) (valeur « f »).</span><span class="sxs-lookup"><span data-stu-id="6349a-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="6349a-293">Une longueur physique doit être maintenue en EMU.</span><span class="sxs-lookup"><span data-stu-id="6349a-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="6349a-294">Une valeur de pixel doit être conservée en tant que nombre entier de pixels.</span><span class="sxs-lookup"><span data-stu-id="6349a-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="6349a-295">Les nombres fractionnaires de pixels ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="6349a-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="6349a-296">Autres représentations</span><span class="sxs-lookup"><span data-stu-id="6349a-296">Alternative representations</span></span>

<span data-ttu-id="6349a-297">Toutes les autres représentations de [fraction](#fraction) et de [longueur](#length) sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="6349a-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="6349a-298">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="6349a-299">angle</span><span class="sxs-lookup"><span data-stu-id="6349a-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="6349a-300">La représentation fondamentale d’un angle est un nombre de degrés multiple de 2 6 (65536) et stocké sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="6349a-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="6349a-301">Étant donné que l’espace de coordonnées est inversé (l’axe des y positif est inactif), un angle horaire est positif.</span><span class="sxs-lookup"><span data-stu-id="6349a-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="6349a-302">Une implémentation conforme est requise pour conserver la précision totale d’une telle valeur.</span><span class="sxs-lookup"><span data-stu-id="6349a-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="6349a-303">Une implémentation est autorisée à utiliser n’importe quelle plage pour les angles et est autorisée à normalise un angle (par exemple, de-180 à + 180 ou de 0 à 360).</span><span class="sxs-lookup"><span data-stu-id="6349a-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="6349a-304">Les implémentations ne doivent pas nécessairement être cohérentes ; Toutefois, la représentation intégrale d’un angle ne doit pas dépasser la plage d’un entier signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6349a-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="6349a-305">Le suffixe FD est utilisé pour identifier cette représentation d’un angle (degré fractionnaire).</span><span class="sxs-lookup"><span data-stu-id="6349a-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="6349a-306">Notez que cela est distingué du suffixe f pour une fraction sans dimension, même si une opération arithmétique identique peut être utilisée pour la prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="6349a-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="6349a-307">La valeur par défaut d’une valeur angulaire est un simple degré, c’est-à-dire une valeur non mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="6349a-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="6349a-308">Cela peut également être signalé par le suffixe «» (le symbole de degré). Toutefois, l’utilisation de cela dépend de la présence d’un encodage de document approprié. par conséquent, le suffixe deg est également défini pour signifier des degrés.</span><span class="sxs-lookup"><span data-stu-id="6349a-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="6349a-309">L’ensemble des suffisants possibles est le suivant.</span><span class="sxs-lookup"><span data-stu-id="6349a-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="6349a-310">Suffixe</span><span class="sxs-lookup"><span data-stu-id="6349a-310">Suffix</span></span>       | <span data-ttu-id="6349a-311">Facteur de conversion</span><span class="sxs-lookup"><span data-stu-id="6349a-311">Conversion Factor</span></span> | <span data-ttu-id="6349a-312">Commentaires</span><span class="sxs-lookup"><span data-stu-id="6349a-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="6349a-313">FD</span><span class="sxs-lookup"><span data-stu-id="6349a-313">fd</span></span>           | <span data-ttu-id="6349a-314">1</span><span class="sxs-lookup"><span data-stu-id="6349a-314">1</span></span>                 | <span data-ttu-id="6349a-315">Représentation interne haute précision</span><span class="sxs-lookup"><span data-stu-id="6349a-315">High-precision internal representation</span></span> |
| <span data-ttu-id="6349a-316">aucun, DEG,</span><span class="sxs-lookup"><span data-stu-id="6349a-316">none, deg,</span></span>   | <span data-ttu-id="6349a-317">65536</span><span class="sxs-lookup"><span data-stu-id="6349a-317">65536</span></span>             | <span data-ttu-id="6349a-318">Degrés</span><span class="sxs-lookup"><span data-stu-id="6349a-318">Degrees</span></span>                                |
| <span data-ttu-id="6349a-319">rad</span><span class="sxs-lookup"><span data-stu-id="6349a-319">rad</span></span>          | <span data-ttu-id="6349a-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="6349a-320">65536pi/180</span></span>       | <span data-ttu-id="6349a-321">Radians</span><span class="sxs-lookup"><span data-stu-id="6349a-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="6349a-322">Autres représentations</span><span class="sxs-lookup"><span data-stu-id="6349a-322">Alternative representations</span></span>

<span data-ttu-id="6349a-323">La transformation de mise à l’échelle présente des discontinuités à des multiples paires de 45.</span><span class="sxs-lookup"><span data-stu-id="6349a-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="6349a-324">C’est pourquoi il est très important que la conversion de toute quantité inexacte soit bien définie.</span><span class="sxs-lookup"><span data-stu-id="6349a-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="6349a-325">Pour cette raison, l’arithmétique de la conversion est définie pour arrondir à moins l’infini.</span><span class="sxs-lookup"><span data-stu-id="6349a-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="6349a-326">Étant donné que cela peut être difficile ou impossible à garantir dans certaines implémentations, l’utilisation des éléments suivants est définie comme une fonctionnalité de niveau 3 :</span><span class="sxs-lookup"><span data-stu-id="6349a-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="6349a-327">Toute valeur de degré fractionnaire.</span><span class="sxs-lookup"><span data-stu-id="6349a-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="6349a-328">Toute valeur en radian</span><span class="sxs-lookup"><span data-stu-id="6349a-328">Any radian value</span></span>

<span data-ttu-id="6349a-329">Par conséquent, les valeurs des valeurs entières FD et Unqualified, ou des valeurs intégrales qualifiées deg ou doivent être gérées exactement par une implémentation de niveau 0 conforme ; Il n’est pas nécessaire d’utiliser d’autres valeurs.</span><span class="sxs-lookup"><span data-stu-id="6349a-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="6349a-330">Il est fortement recommandé que toute implémentation traite la conversion d’une valeur de degré fractionnaire en valeur de degré mis à l’échelle (FD) exactement.</span><span class="sxs-lookup"><span data-stu-id="6349a-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="6349a-331">Cela peut être effectué sans prise en charge de la virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="6349a-331">This can be done without floating point support.</span></span>

<span data-ttu-id="6349a-332">Les exigences plus précises pour la conversion distinguent FD de f.</span><span class="sxs-lookup"><span data-stu-id="6349a-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="6349a-333">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="6349a-334">color</span><span class="sxs-lookup"><span data-stu-id="6349a-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="6349a-335">Les couleurs constituent une partie essentielle des graphiques modernes des ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="6349a-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="6349a-336">La proposition utilise les méthodes établies pour spécifier des couleurs fixes.</span><span class="sxs-lookup"><span data-stu-id="6349a-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="6349a-337">Toutefois, les couleurs des diagrammes sont rarement des couleurs statiques simples ; elles sont souvent dérivées d’autres éléments du diagramme.</span><span class="sxs-lookup"><span data-stu-id="6349a-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="6349a-338">La plupart de ces informations sont propres à l’application. cette proposition fournit donc deux mécanismes très basiques pour spécifier un tel comportement :</span><span class="sxs-lookup"><span data-stu-id="6349a-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="6349a-339">Une couleur peut être dérivée d’une autre couleur dans la même forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="6349a-340">Un petit nombre d’opérations arithmétiques sont définies pour la dérivation ou la modification d’une couleur.</span><span class="sxs-lookup"><span data-stu-id="6349a-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="6349a-341">Le mécanisme de forme prototype complète cela en autorisant la définition de prototypes à partir desquels les couleurs peuvent être héritées.</span><span class="sxs-lookup"><span data-stu-id="6349a-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="6349a-342">Une valeur de couleur est un sur-ensemble de la [définition de couleur CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="6349a-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="6349a-343">Les extensions permettent de déterminer la valeur de couleur RVB à partir d’autres couleurs dans la forme ou à partir d’un modèle de couleurs global défini à l’aide de CSS1.</span><span class="sxs-lookup"><span data-stu-id="6349a-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="6349a-344">Si la valeur d’un élément est définie comme une couleur, le *contenu* d’un élément définit la valeur de couleur au moyen d’un jeton de couleur unique éventuellement modifié par une opération arithmétique sur la couleur RVB correspondante.</span><span class="sxs-lookup"><span data-stu-id="6349a-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="6349a-345">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="6349a-346">Unités de couleur</span><span class="sxs-lookup"><span data-stu-id="6349a-346">Color units</span></span>

<span data-ttu-id="6349a-347">L’ensemble complet des jetons de couleur provient de diverses sources : HTML, CSS1 et cette proposition.</span><span class="sxs-lookup"><span data-stu-id="6349a-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="6349a-348">Ils sont définis comme suit à l’aide de la notation de [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) ou de la notation XPointer définie pour la liaison XML.</span><span class="sxs-lookup"><span data-stu-id="6349a-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="6349a-349">Dans les définitions XPointer, la source d’emplacement est l’élément contenant la valeur de couleur, et l’expression fait référence au jeu d’éléments entier de la forme comme si des éléments de prototype de base avaient été fusionnés avec la forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="6349a-350">Lorsque l’élément correspondant n’existe pas, la valeur par défaut de cet élément est utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="6349a-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="6349a-351">Couleur</span><span class="sxs-lookup"><span data-stu-id="6349a-351">Color</span></span>            | <span data-ttu-id="6349a-352">Définition</span><span class="sxs-lookup"><span data-stu-id="6349a-352">Definition</span></span>                                                                                                  | <span data-ttu-id="6349a-353">Level</span><span class="sxs-lookup"><span data-stu-id="6349a-353">Level</span></span> | <span data-ttu-id="6349a-354">Description</span><span class="sxs-lookup"><span data-stu-id="6349a-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6349a-355">name</span><span class="sxs-lookup"><span data-stu-id="6349a-355">name</span></span>             | <span data-ttu-id="6349a-356">Voir ci-dessous</span><span class="sxs-lookup"><span data-stu-id="6349a-356">See below</span></span>                                                                                                   | <span data-ttu-id="6349a-357">0</span><span class="sxs-lookup"><span data-stu-id="6349a-357">0</span></span>     | <span data-ttu-id="6349a-358">Nom de la couleur HTML, comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6349a-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="6349a-359">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="6349a-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="6349a-360">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="6349a-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="6349a-361">0</span><span class="sxs-lookup"><span data-stu-id="6349a-361">0</span></span>     | <span data-ttu-id="6349a-362">Représentation de couleur standard CSS1/sRVB utilisant des valeurs de la plage 0.. 255 représentées à l’aide de 2 chiffres hexadécimaux chacun.</span><span class="sxs-lookup"><span data-stu-id="6349a-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="6349a-363">\#composantes</span><span class="sxs-lookup"><span data-stu-id="6349a-363">\#rgb</span></span>            | <span data-ttu-id="6349a-364">\#RRGGBB</span><span class="sxs-lookup"><span data-stu-id="6349a-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="6349a-365">1</span><span class="sxs-lookup"><span data-stu-id="6349a-365">1</span></span>     | <span data-ttu-id="6349a-366">Formulaire CSS1 abrégé avec seulement trois chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="6349a-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="6349a-367">RGB (r, g, b)</span><span class="sxs-lookup"><span data-stu-id="6349a-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="6349a-368">\#r activée p</span><span class="sxs-lookup"><span data-stu-id="6349a-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="6349a-369">1</span><span class="sxs-lookup"><span data-stu-id="6349a-369">1</span></span>     | <span data-ttu-id="6349a-370">Forme CSS1 RGB ; les éléments de la valeur RVB sont convertis comme défini dans [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="6349a-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="6349a-371">fill</span><span class="sxs-lookup"><span data-stu-id="6349a-371">fill</span></span>             | <span data-ttu-id="6349a-372">ancêtre (1, forme)</span><span class="sxs-lookup"><span data-stu-id="6349a-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="6349a-373">enfant (1, remplissage)</span><span class="sxs-lookup"><span data-stu-id="6349a-373">child(1, fill)</span></span><br/> <span data-ttu-id="6349a-374">enfant (1, couleur)</span><span class="sxs-lookup"><span data-stu-id="6349a-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="6349a-375">1</span><span class="sxs-lookup"><span data-stu-id="6349a-375">1</span></span>     | <span data-ttu-id="6349a-376">Couleur de remplissage de premier plan de la forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="6349a-377">fillBack</span><span class="sxs-lookup"><span data-stu-id="6349a-377">fillBack</span></span>         | <span data-ttu-id="6349a-378">ancêtre (1, forme)</span><span class="sxs-lookup"><span data-stu-id="6349a-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="6349a-379">enfant (1, remplissage)</span><span class="sxs-lookup"><span data-stu-id="6349a-379">child(1, fill)</span></span><br/> <span data-ttu-id="6349a-380">enfant (1, précédent)</span><span class="sxs-lookup"><span data-stu-id="6349a-380">child(1, back)</span></span><br/> <span data-ttu-id="6349a-381">enfant (1, couleur)</span><span class="sxs-lookup"><span data-stu-id="6349a-381">child(1, color)</span></span><br/> | <span data-ttu-id="6349a-382">1</span><span class="sxs-lookup"><span data-stu-id="6349a-382">1</span></span>     | <span data-ttu-id="6349a-383">Couleur d’arrière-plan du remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="6349a-384">line</span><span class="sxs-lookup"><span data-stu-id="6349a-384">line</span></span>             | <span data-ttu-id="6349a-385">ancêtre (1, forme)</span><span class="sxs-lookup"><span data-stu-id="6349a-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="6349a-386">enfant (1, ligne)</span><span class="sxs-lookup"><span data-stu-id="6349a-386">child(1, line)</span></span><br/> <span data-ttu-id="6349a-387">enfant (1, couleur)</span><span class="sxs-lookup"><span data-stu-id="6349a-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="6349a-388">1</span><span class="sxs-lookup"><span data-stu-id="6349a-388">1</span></span>     | <span data-ttu-id="6349a-389">Couleur de la ligne de premier plan de la forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="6349a-390">lineBack</span><span class="sxs-lookup"><span data-stu-id="6349a-390">lineBack</span></span>         | <span data-ttu-id="6349a-391">ancêtre (1, forme)</span><span class="sxs-lookup"><span data-stu-id="6349a-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="6349a-392">enfant (1, ligne)</span><span class="sxs-lookup"><span data-stu-id="6349a-392">child(1, line)</span></span><br/> <span data-ttu-id="6349a-393">enfant (1, précédent)</span><span class="sxs-lookup"><span data-stu-id="6349a-393">child(1,back)</span></span> <br/> <span data-ttu-id="6349a-394">enfant (1, couleur)</span><span class="sxs-lookup"><span data-stu-id="6349a-394">child(1, color)</span></span><br/> | <span data-ttu-id="6349a-395">1</span><span class="sxs-lookup"><span data-stu-id="6349a-395">1</span></span>     | <span data-ttu-id="6349a-396">Couleur de ligne d’arrière-plan de la forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="6349a-397">lineOrFill</span><span class="sxs-lookup"><span data-stu-id="6349a-397">lineOrFill</span></span>       | <span data-ttu-id="6349a-398">trait, remplissage</span><span class="sxs-lookup"><span data-stu-id="6349a-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="6349a-399">1</span><span class="sxs-lookup"><span data-stu-id="6349a-399">1</span></span>     | <span data-ttu-id="6349a-400">Valeur de ligne si elle n’est pas définie par défaut ; sinon, la valeur de remplissage.</span><span class="sxs-lookup"><span data-stu-id="6349a-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="6349a-401">Cela retourne effectivement la couleur qui se trouve à l’extrémité de la forme.</span><span class="sxs-lookup"><span data-stu-id="6349a-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="6349a-402">fillThenLine</span><span class="sxs-lookup"><span data-stu-id="6349a-402">fillThenLine</span></span>     | <span data-ttu-id="6349a-403">remplissage, ligne</span><span class="sxs-lookup"><span data-stu-id="6349a-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="6349a-404">1</span><span class="sxs-lookup"><span data-stu-id="6349a-404">1</span></span>     | <span data-ttu-id="6349a-405">Valeur de remplissage si elle n’est pas définie par défaut ; sinon, la valeur de ligne.</span><span class="sxs-lookup"><span data-stu-id="6349a-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="6349a-406">Cela renvoie effectivement la couleur principale de la forme (si la forme n’est pas remplie, le résultat est la couleur de ligne).</span><span class="sxs-lookup"><span data-stu-id="6349a-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="6349a-407">shadow</span><span class="sxs-lookup"><span data-stu-id="6349a-407">shadow</span></span>           | <span data-ttu-id="6349a-408">ancêtre (1, forme)</span><span class="sxs-lookup"><span data-stu-id="6349a-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="6349a-409">enfant (1, ombre)</span><span class="sxs-lookup"><span data-stu-id="6349a-409">child(1, shadow)</span></span><br/> <span data-ttu-id="6349a-410">enfant (1, couleur)</span><span class="sxs-lookup"><span data-stu-id="6349a-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="6349a-411">2</span><span class="sxs-lookup"><span data-stu-id="6349a-411">2</span></span>     | <span data-ttu-id="6349a-412">Couleur de l’ombre (il s’agit d’une fonctionnalité de niveau 2).</span><span class="sxs-lookup"><span data-stu-id="6349a-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="6349a-413">scheme</span><span class="sxs-lookup"><span data-stu-id="6349a-413">scheme</span></span>           | <span data-ttu-id="6349a-414">Voir ci-dessous</span><span class="sxs-lookup"><span data-stu-id="6349a-414">See below</span></span>                                                                                                   | <span data-ttu-id="6349a-415">1</span><span class="sxs-lookup"><span data-stu-id="6349a-415">1</span></span>     | <span data-ttu-id="6349a-416">Couleur de schéma du schéma défini pour le document ; Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6349a-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="6349a-417">Scheme (*index*)</span><span class="sxs-lookup"><span data-stu-id="6349a-417">scheme(*index*)</span></span>  | <span data-ttu-id="6349a-418">Voir ci-dessous</span><span class="sxs-lookup"><span data-stu-id="6349a-418">See below</span></span>                                                                                                   | <span data-ttu-id="6349a-419">1</span><span class="sxs-lookup"><span data-stu-id="6349a-419">1</span></span>     | <span data-ttu-id="6349a-420">*Index* de couleurs du modèle, à partir de 0 ; Voir ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6349a-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="6349a-421">this</span><span class="sxs-lookup"><span data-stu-id="6349a-421">this</span></span>             | <span data-ttu-id="6349a-422">Découle</span><span class="sxs-lookup"><span data-stu-id="6349a-422">Implied</span></span>                                                                                                     | <span data-ttu-id="6349a-423">2</span><span class="sxs-lookup"><span data-stu-id="6349a-423">2</span></span>     | <span data-ttu-id="6349a-424">L’opération (remplissage d’un tracé ou dessin) est définie d’une autre façon (par exemple, en tant que bitmap), et la couleur spécifie une « modification » des couleurs, de cette façon.</span><span class="sxs-lookup"><span data-stu-id="6349a-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="6349a-425">palette (*index*)</span><span class="sxs-lookup"><span data-stu-id="6349a-425">palette(*index*)</span></span> | <span data-ttu-id="6349a-426">Découle</span><span class="sxs-lookup"><span data-stu-id="6349a-426">Implied</span></span>                                                                                                     | <span data-ttu-id="6349a-427">3</span><span class="sxs-lookup"><span data-stu-id="6349a-427">3</span></span>     | <span data-ttu-id="6349a-428">Se comporte de la même façon que cela, sauf qu’une seule entrée dans une table de couleurs de bitmap est identifiée.</span><span class="sxs-lookup"><span data-stu-id="6349a-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="6349a-429">Autorisé uniquement lorsque l’énoncé explicite est spécifié.</span><span class="sxs-lookup"><span data-stu-id="6349a-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="6349a-430">aucun</span><span class="sxs-lookup"><span data-stu-id="6349a-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="6349a-431">2</span><span class="sxs-lookup"><span data-stu-id="6349a-431">2</span></span>     | <span data-ttu-id="6349a-432">Indique l’absence d’une couleur ; peut être utilisé pour annuler une opération de dessin qui utilise la couleur.</span><span class="sxs-lookup"><span data-stu-id="6349a-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="6349a-433">système</span><span class="sxs-lookup"><span data-stu-id="6349a-433">system</span></span>           | <span data-ttu-id="6349a-434">Voir ci-dessous</span><span class="sxs-lookup"><span data-stu-id="6349a-434">See below</span></span>                                                                                                   | <span data-ttu-id="6349a-435">3</span><span class="sxs-lookup"><span data-stu-id="6349a-435">3</span></span>     | <span data-ttu-id="6349a-436">Couleur définie par l’interface utilisateur système.</span><span class="sxs-lookup"><span data-stu-id="6349a-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="6349a-437">La couleur This permet à une valeur de couleur de spécifier une modification d’une couleur qui est dérivée d’une autre façon. en particulier, une seule opération peut être spécifiée pour toutes les couleurs d’une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6349a-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="6349a-438">La couleur palette (*index*) identifie une entrée particulière dans une image bitmap mappée à la palette.</span><span class="sxs-lookup"><span data-stu-id="6349a-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="6349a-439">L’utilisation de cet élément est uniquement définie pour l’enregistrement d’une entrée de table de couleurs qui doit être considérée comme transparente dans une telle image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6349a-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="6349a-440">La définition d’une valeur de couleur ne doit pas faire référence à elle-même, directement ou indirectement.</span><span class="sxs-lookup"><span data-stu-id="6349a-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="6349a-441">Si une telle définition est rencontrée, il est recommandé, mais pas obligatoire, que l’implémentation traite la valeur indéfinie comme étant noire.</span><span class="sxs-lookup"><span data-stu-id="6349a-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="6349a-442">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="6349a-443">Couleurs HTML</span><span class="sxs-lookup"><span data-stu-id="6349a-443">HTML colors</span></span>

<span data-ttu-id="6349a-444">Le [code html](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) définit les seize noms de couleurs suivants :</span><span class="sxs-lookup"><span data-stu-id="6349a-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="6349a-445">Noms de couleurs et valeurs sRVB</span><span class="sxs-lookup"><span data-stu-id="6349a-445">Color names and sRGB values</span></span>

![Exemple de couleur noire.](images/black.gif)

<span data-ttu-id="6349a-447">Black = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="6349a-447">Black = "\#000000"</span></span>

![Exemple de couleur verte.](images/green.gif)

<span data-ttu-id="6349a-449">Vert = « \# 008000 »</span><span class="sxs-lookup"><span data-stu-id="6349a-449">Green = "\#008000"</span></span>

![Exemple de couleur Silver.](images/silver.gif)

<span data-ttu-id="6349a-451">Silver = « \# C0C0C0 »</span><span class="sxs-lookup"><span data-stu-id="6349a-451">Silver = "\#C0C0C0"</span></span>

![Exemple de couleur citron.](images/lime.gif)

<span data-ttu-id="6349a-453">Citron = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="6349a-453">Lime = "\#00FF00"</span></span>

![Exemple de couleur grise.](images/gray.gif)

<span data-ttu-id="6349a-455">Gray = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="6349a-455">Gray = "\#808080"</span></span>

![Exemple de couleur d’olive.](images/olive.gif)

<span data-ttu-id="6349a-457">Olive = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="6349a-457">Olive = "\#808000"</span></span>

![Exemple de couleur blanche.](images/white.gif)

<span data-ttu-id="6349a-459">Blanc = " \# FFFFFF"</span><span class="sxs-lookup"><span data-stu-id="6349a-459">White = "\#FFFFFF"</span></span>

![Exemple de couleur ywllow.](images/yellow.gif)

<span data-ttu-id="6349a-461">Yellow = " \# FFFF00"</span><span class="sxs-lookup"><span data-stu-id="6349a-461">Yellow = "\#FFFF00"</span></span>

![Exemple de couleur marron.](images/maroon.gif)

<span data-ttu-id="6349a-463">Marron = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="6349a-463">Maroon = "\#800000"</span></span>

![Exemple de couleur marine.](images/navy.gif)

<span data-ttu-id="6349a-465">Bleu foncé = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="6349a-465">Navy = "\#000080"</span></span>

![Exemple de couleur rouge.](images/red.gif)

<span data-ttu-id="6349a-467">Rouge = « \# FF0000 »</span><span class="sxs-lookup"><span data-stu-id="6349a-467">Red = "\#FF0000"</span></span>

![Exemple de couleur bleue.](images/blue.gif)

<span data-ttu-id="6349a-469">Blue = « \# 0000FF »</span><span class="sxs-lookup"><span data-stu-id="6349a-469">Blue = "\#0000FF"</span></span>

![Exemple de couleur violette.](images/purple.gif)

<span data-ttu-id="6349a-471">Violet = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="6349a-471">Purple = "\#800080"</span></span>

![Exemple de couleur bleu-vert.](images/teal.gif)

<span data-ttu-id="6349a-473">Bleu-vert = « \# 008080 »</span><span class="sxs-lookup"><span data-stu-id="6349a-473">Teal = "\#008080"</span></span>

![Exemple de couleur fuchsia.](images/fuchsia.gif)

<span data-ttu-id="6349a-475">Fuchsia = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="6349a-475">Fuchsia = "\#FF00FF"</span></span>

![Exemple de couleur cyan.](images/aqua.gif)

<span data-ttu-id="6349a-477">Cyan = « \# 00FFFF »</span><span class="sxs-lookup"><span data-stu-id="6349a-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="6349a-478">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="6349a-479">Couleurs du schéma</span><span class="sxs-lookup"><span data-stu-id="6349a-479">Scheme colors</span></span>

<span data-ttu-id="6349a-480">Les couleurs de schéma référencées par le modèle sont définies au niveau du document à l’aide de la balise méta avec l’attribut de nom « jeu de couleurs de thème ».</span><span class="sxs-lookup"><span data-stu-id="6349a-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="6349a-481">Cette balise permet de définir jusqu’à huit couleurs de schéma.</span><span class="sxs-lookup"><span data-stu-id="6349a-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="6349a-482">Les couleurs non définies doivent par défaut être noires.</span><span class="sxs-lookup"><span data-stu-id="6349a-482">Undefined colors should default to black.</span></span> <span data-ttu-id="6349a-483">Les couleurs du schéma permettent de modifier le jeu de couleurs utilisé pour un document complet simplement en modifiant le contenu du jeu de couleurs du thème.</span><span class="sxs-lookup"><span data-stu-id="6349a-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="6349a-484">Pour vous assurer que les graphiques importés à partir de différentes applications de création utilisent de manière cohérente les couleurs du schéma, les interprétations suivantes sont définies.</span><span class="sxs-lookup"><span data-stu-id="6349a-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="6349a-485">« Utilisation » est une brève description de l’objectif et la colonne « Description » fournit des détails supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6349a-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="6349a-486">Index</span><span class="sxs-lookup"><span data-stu-id="6349a-486">Index</span></span> | <span data-ttu-id="6349a-487">Nom</span><span class="sxs-lookup"><span data-stu-id="6349a-487">Name</span></span>              | <span data-ttu-id="6349a-488">Usage</span><span class="sxs-lookup"><span data-stu-id="6349a-488">Usage</span></span>                         | <span data-ttu-id="6349a-489">Description</span><span class="sxs-lookup"><span data-stu-id="6349a-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6349a-490">0</span><span class="sxs-lookup"><span data-stu-id="6349a-490">0</span></span>     | <span data-ttu-id="6349a-491">Scheme. Background</span><span class="sxs-lookup"><span data-stu-id="6349a-491">scheme.background</span></span> | <span data-ttu-id="6349a-492">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6349a-492">Background</span></span>                    | <span data-ttu-id="6349a-493">Couleur utilisée pour l’arrière-plan d’un graphique (et, souvent, pour la page entière).</span><span class="sxs-lookup"><span data-stu-id="6349a-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="6349a-494">1</span><span class="sxs-lookup"><span data-stu-id="6349a-494">1</span></span>     | <span data-ttu-id="6349a-495">Scheme. Text</span><span class="sxs-lookup"><span data-stu-id="6349a-495">scheme.text</span></span>       | <span data-ttu-id="6349a-496">Texte et lignes</span><span class="sxs-lookup"><span data-stu-id="6349a-496">Text and lines</span></span>                | <span data-ttu-id="6349a-497">Couleur du texte attaché à une forme et la couleur de ligne standard.</span><span class="sxs-lookup"><span data-stu-id="6349a-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="6349a-498">2</span><span class="sxs-lookup"><span data-stu-id="6349a-498">2</span></span>     | <span data-ttu-id="6349a-499">schéma. Shadow</span><span class="sxs-lookup"><span data-stu-id="6349a-499">scheme.shadow</span></span>     | <span data-ttu-id="6349a-500">Ombres</span><span class="sxs-lookup"><span data-stu-id="6349a-500">Shadows</span></span>                       | <span data-ttu-id="6349a-501">Couleur de l’ombre standard : couleur généralement utilisée pour les ombres des formes.</span><span class="sxs-lookup"><span data-stu-id="6349a-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="6349a-502">3</span><span class="sxs-lookup"><span data-stu-id="6349a-502">3</span></span>     | <span data-ttu-id="6349a-503">Scheme. title</span><span class="sxs-lookup"><span data-stu-id="6349a-503">scheme.title</span></span>      | <span data-ttu-id="6349a-504">Texte du titre</span><span class="sxs-lookup"><span data-stu-id="6349a-504">Title text</span></span>                    | <span data-ttu-id="6349a-505">Couleur à utiliser pour le titre ou le texte du titre.</span><span class="sxs-lookup"><span data-stu-id="6349a-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="6349a-506">4</span><span class="sxs-lookup"><span data-stu-id="6349a-506">4</span></span>     | <span data-ttu-id="6349a-507">Scheme. Fill</span><span class="sxs-lookup"><span data-stu-id="6349a-507">scheme.fill</span></span>       | <span data-ttu-id="6349a-508">Remplit</span><span class="sxs-lookup"><span data-stu-id="6349a-508">Fills</span></span>                         | <span data-ttu-id="6349a-509">Couleur de remplissage standard : couleur généralement utilisée pour remplir les formes.</span><span class="sxs-lookup"><span data-stu-id="6349a-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="6349a-510">5</span><span class="sxs-lookup"><span data-stu-id="6349a-510">5</span></span>     | <span data-ttu-id="6349a-511">Scheme. accent</span><span class="sxs-lookup"><span data-stu-id="6349a-511">scheme.accent</span></span>     | <span data-ttu-id="6349a-512">Non</span><span class="sxs-lookup"><span data-stu-id="6349a-512">Accent</span></span>                        | <span data-ttu-id="6349a-513">Couleur de mise en surbrillance normale utilisée pour mettre en relief un élément important d’un graphique.</span><span class="sxs-lookup"><span data-stu-id="6349a-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="6349a-514">6</span><span class="sxs-lookup"><span data-stu-id="6349a-514">6</span></span>     | <span data-ttu-id="6349a-515">Scheme. HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="6349a-515">scheme.hyperlink</span></span>  | <span data-ttu-id="6349a-516">Accent et lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="6349a-516">Accent and hyperlink</span></span>          | <span data-ttu-id="6349a-517">Couleur de surbrillance utilisée pour les liens hypertexte.</span><span class="sxs-lookup"><span data-stu-id="6349a-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="6349a-518">Peut être utilisé à d’autres fins lorsque la couleur désigne un lien vers d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="6349a-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="6349a-519">7</span><span class="sxs-lookup"><span data-stu-id="6349a-519">7</span></span>     | <span data-ttu-id="6349a-520">schéma. suivi</span><span class="sxs-lookup"><span data-stu-id="6349a-520">scheme.followed</span></span>   | <span data-ttu-id="6349a-521">Accent et lien hypertexte visité</span><span class="sxs-lookup"><span data-stu-id="6349a-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="6349a-522">Couleur de surbrillance pour les liens hypertexte visités ; également adapté aux liens « en arrière ».</span><span class="sxs-lookup"><span data-stu-id="6349a-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="6349a-523">Une couleur de schéma peut être référencée par son nom ou par son index, de sorte que Scheme. Fill et Scheme (4) sont de la même couleur.</span><span class="sxs-lookup"><span data-stu-id="6349a-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="6349a-524">Les couleurs de schéma ne participent pas au schéma par défaut si aucune couleur n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6349a-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="6349a-525">Une couleur de remplissage non spécifiée doit toujours être interprétée en tant que blanc, quelle que soit la couleur du jeu de couleurs 4.</span><span class="sxs-lookup"><span data-stu-id="6349a-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="6349a-526">Les couleurs « accent » doivent être contrastées avec les couleurs d’arrière-plan (0) et de remplissage (4), tandis que les couleurs de texte et de texte du titre doivent avoir la même propriété.</span><span class="sxs-lookup"><span data-stu-id="6349a-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="6349a-527">Une technique standard consiste à rendre les accents colorés et le texte standard non coloré (généralement en noir ou blanc).</span><span class="sxs-lookup"><span data-stu-id="6349a-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="6349a-528">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="6349a-529">Couleurs système</span><span class="sxs-lookup"><span data-stu-id="6349a-529">System colors</span></span>

<span data-ttu-id="6349a-530">Les applications enregistrent parfois des couleurs en fonction des paramètres du système d’exploitation dans les graphiques.</span><span class="sxs-lookup"><span data-stu-id="6349a-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="6349a-531">Normalement, ceux-ci sont temporaires et n’ont pas besoin d’être écrits ; les définitions thesystemcolor existent uniquement pour prendre en charge cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6349a-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="6349a-532">Une couleur système est introduite en définissant une balise appropriée dans un nouvel espace de noms et en insérant les informations appropriées dans le contenu de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6349a-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="6349a-533">Cette proposition définit une telle balise pour encoder les couleurs de l’interface utilisateur Windows définies dans le fichier d’en-tête winuser. h.</span><span class="sxs-lookup"><span data-stu-id="6349a-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="6349a-534">Le contenu de l’élément est un entier unique qui contient la valeur de la définition de couleur appropriée \_ de winuser. h.</span><span class="sxs-lookup"><span data-stu-id="6349a-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="6349a-535">Une technique similaire peut être adoptée pour toute spécification de couleur propre au système ou à l’application.</span><span class="sxs-lookup"><span data-stu-id="6349a-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="6349a-536">Il est fortement recommandé d’utiliser cette fonctionnalité uniquement pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="6349a-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="6349a-537">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="6349a-538">Couleurs pures</span><span class="sxs-lookup"><span data-stu-id="6349a-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="6349a-539">Si l’élément <pure/> apparaît dans une valeur de couleur, il s’agit d’une indication que la couleur ne doit pas être approximative par un modèle de trame.</span><span class="sxs-lookup"><span data-stu-id="6349a-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="6349a-540">Il s’agit d’une fonctionnalité de niveau 1, et une implémentation conforme n’a pas besoin d’être respectée.</span><span class="sxs-lookup"><span data-stu-id="6349a-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="6349a-541">La désignation est importante pour les graphiques affichés sur des appareils de résolution moyenne, tels que les affichages vidéo, où les petites fonctionnalités (telles que les lignes) peuvent provoquer des alias erronés avec des couleurs dépendantes.</span><span class="sxs-lookup"><span data-stu-id="6349a-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="6349a-542">Sur les appareils tels que les imprimantes, qui déforment normalement toutes les couleurs, à l’exception des quelques couleurs entièrement saturées, le tramage est normalement suffisamment suffisant pour éviter ce problème.</span><span class="sxs-lookup"><span data-stu-id="6349a-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="6349a-543">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="6349a-544">Réglages des couleurs</span><span class="sxs-lookup"><span data-stu-id="6349a-544">Color adjustments</span></span>

<span data-ttu-id="6349a-545">La couleur de base peut être ajustée par des opérations arithmétiques sur la valeur RVB.</span><span class="sxs-lookup"><span data-stu-id="6349a-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="6349a-546">Ces opérations sont définies à l’aide d’éléments supplémentaires dans la valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="6349a-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="6349a-547">De tels ajustements sont utiles uniquement lorsqu’ils sont appliqués à des couleurs dérivées d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="6349a-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="6349a-548">Il est possible de spécifier un tel ajustement sur une valeur de couleur fixe ; Toutefois, une implémentation est autorisée à réduire cela à la valeur RVB correspondante et à la stocker à la place de l’original.</span><span class="sxs-lookup"><span data-stu-id="6349a-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="6349a-549">Toutes les fonctionnalités de réglage des couleurs décrites dans cette section sont des fonctionnalités de niveau 1.</span><span class="sxs-lookup"><span data-stu-id="6349a-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="6349a-550">Le paramètre des six premières opérations est une valeur numérique intégrale unique comprise entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="6349a-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="6349a-551">L’ajustement est effectué sur la valeur RGB 3x8bit comme suit :</span><span class="sxs-lookup"><span data-stu-id="6349a-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="6349a-552">Si <gray/> est spécifié, la valeur RVB est remplacée par YYY, où y est la valeur de luminance (y) calculée à partir de la valeur sRVB en suivant l’ITU-r BT. 709.</span><span class="sxs-lookup"><span data-stu-id="6349a-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="6349a-553">Ce calcul est le suivant :</span><span class="sxs-lookup"><span data-stu-id="6349a-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="6349a-554">Si une modification Color. op est donnée, chaque composant est ajusté séparément en fonction du tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6349a-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="6349a-555">c est la valeur du composant, et p est la valeur Color. Parameter.</span><span class="sxs-lookup"><span data-stu-id="6349a-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="6349a-556">Opération</span><span class="sxs-lookup"><span data-stu-id="6349a-556">Operation</span></span>       | <span data-ttu-id="6349a-557">Formule</span><span class="sxs-lookup"><span data-stu-id="6349a-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="6349a-558">fonce</span><span class="sxs-lookup"><span data-stu-id="6349a-558">darken</span></span>          | <span data-ttu-id="6349a-559">c : = CXP/255</span><span class="sxs-lookup"><span data-stu-id="6349a-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="6349a-560">Light</span><span class="sxs-lookup"><span data-stu-id="6349a-560">lighten</span></span>         | <span data-ttu-id="6349a-561">c : = 255-(255-c) XP/255</span><span class="sxs-lookup"><span data-stu-id="6349a-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="6349a-562">add</span><span class="sxs-lookup"><span data-stu-id="6349a-562">add</span></span>             | <span data-ttu-id="6349a-563">c : = c + p</span><span class="sxs-lookup"><span data-stu-id="6349a-563">c := c + p</span></span>                         |
    | <span data-ttu-id="6349a-564">soustraction</span><span class="sxs-lookup"><span data-stu-id="6349a-564">subtract</span></span>        | <span data-ttu-id="6349a-565">c : = c-p</span><span class="sxs-lookup"><span data-stu-id="6349a-565">c := c - p</span></span>                         |
    | <span data-ttu-id="6349a-566">reversesubtract</span><span class="sxs-lookup"><span data-stu-id="6349a-566">reversesubtract</span></span> | <span data-ttu-id="6349a-567">c : = p-c</span><span class="sxs-lookup"><span data-stu-id="6349a-567">c := p - c</span></span>                         |
    | <span data-ttu-id="6349a-568">blackwhite</span><span class="sxs-lookup"><span data-stu-id="6349a-568">blackwhite</span></span>      | <span data-ttu-id="6349a-569">Si c < p thenc : = 0elsec : = 255</span><span class="sxs-lookup"><span data-stu-id="6349a-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="6349a-570">Dans chaque cas, si la valeur du composant calculé, c, est supérieure à 255, 255 est utilisé et, s’il est inférieur à 0, la valeur 0 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="6349a-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="6349a-571">Si <INVERT128/> est donné, la valeur 128 est soustraite ou ajoutée à chaque composant selon que le composant est inférieur à 128 ou non.</span><span class="sxs-lookup"><span data-stu-id="6349a-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="6349a-572">Si <invert/> est donné, chaque composant est remplacé par 255 moins la valeur du composant.</span><span class="sxs-lookup"><span data-stu-id="6349a-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="6349a-573">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="6349a-574">son</span><span class="sxs-lookup"><span data-stu-id="6349a-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="6349a-575">Une police est identifiée à l’aide d’un attribut de style tel que défini dans la [section CSS1 5,2 (propriétés de police)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span><span class="sxs-lookup"><span data-stu-id="6349a-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="6349a-576">Le corps de l’élément de police est, à l’heure actuelle, non défini, mais peut être utilisé à l’avenir pour encoder les informations de police standard.</span><span class="sxs-lookup"><span data-stu-id="6349a-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="6349a-577">Les implémentations initiales de cette proposition doivent conserver les informations, mais pas les interpréter.</span><span class="sxs-lookup"><span data-stu-id="6349a-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="6349a-578">Il est concevable que la prise en charge soit ajoutée à l’avenir pour les informations de police hors ligne (polices téléchargeables ou ressources de police partagées).</span><span class="sxs-lookup"><span data-stu-id="6349a-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="6349a-579">Cette opération est effectuée par un élément de lien XML dans le contenu de l’élément font, garantissant la compatbility descendante avec les implémentations initiales.</span><span class="sxs-lookup"><span data-stu-id="6349a-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="6349a-580">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="6349a-581">bitmap</span><span class="sxs-lookup"><span data-stu-id="6349a-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="6349a-582">L’élément bitmap autorise une référence à une ressource d’image hors ligne (normalement une image bitmap) à inclure dans un graphique.</span><span class="sxs-lookup"><span data-stu-id="6349a-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="6349a-583">la bitmap est une fonctionnalité de niveau 1.</span><span class="sxs-lookup"><span data-stu-id="6349a-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="6349a-584">L’attribut Behavior peut être utilisé pour indiquer comment la bitmap doit être gérée par une application de modification.</span><span class="sxs-lookup"><span data-stu-id="6349a-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="6349a-585">La valeur peut être l’un des jetons suivants (ou les deux).</span><span class="sxs-lookup"><span data-stu-id="6349a-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="6349a-586">par jeton</span><span class="sxs-lookup"><span data-stu-id="6349a-586">Token</span></span>    | <span data-ttu-id="6349a-587">Description</span><span class="sxs-lookup"><span data-stu-id="6349a-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6349a-588">séparé</span><span class="sxs-lookup"><span data-stu-id="6349a-588">separate</span></span> | <span data-ttu-id="6349a-589">Marque l’image bitmap comme une entité distincte, qui ne doit pas être considérée comme une partie intégrante du document.</span><span class="sxs-lookup"><span data-stu-id="6349a-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="6349a-590">L’image bitmap ne doit pas être conservée avec le document.</span><span class="sxs-lookup"><span data-stu-id="6349a-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="6349a-591">Si le document est copié, l’image bitmap ne doit pas être copiée ; Si le document est déplacé, l’image bitmap ne doit pas être déplacée.</span><span class="sxs-lookup"><span data-stu-id="6349a-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="6349a-592">ressource d’origine</span><span class="sxs-lookup"><span data-stu-id="6349a-592">original</span></span> | <span data-ttu-id="6349a-593">L’attribut title identifie l’emplacement d’origine de l’image bitmap comme une URL ; dans le cas contraire, la signification du titre n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6349a-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="6349a-594">Ces valeurs sont à la fois des indications sur le comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="6349a-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="6349a-595">L’option distinct fait référence au comportement des données référencées par href.</span><span class="sxs-lookup"><span data-stu-id="6349a-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="6349a-596">Si les deux éléments sont distincts et originaux, l’application est censée ignorer l’URI href et régénérer l’image bitmap à partir des données d’origine.</span><span class="sxs-lookup"><span data-stu-id="6349a-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="6349a-597">Si seul l’original est donné, l’application est censée utiliser l’URI href pour trouver la bitmap, mais peut donner à l’utilisateur la possibilité de la régénérer.</span><span class="sxs-lookup"><span data-stu-id="6349a-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="6349a-598">Il est possible de donner à l’URI href et à l’attribut title la même valeur (lexicale), ce qui est approprié si le bitmap référencé n’est pas « stocké avec » dans le document.</span><span class="sxs-lookup"><span data-stu-id="6349a-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="6349a-599">Il est prévu (même s’il n’est pas obligatoire) que href soit utilisé pour la copie de l’image bitmap du document, qui peut être supprimé si les formes de référence sont supprimées, et que ce titre doit être utilisé pour indiquer une copie partagée.</span><span class="sxs-lookup"><span data-stu-id="6349a-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="6349a-600">Par conséquent, si les deux contiennent la même valeur, il n’y a pas de copie spécifique au document.</span><span class="sxs-lookup"><span data-stu-id="6349a-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="6349a-601">Les applications peuvent ignorer l’indication si elles ne tiennent pas dans le modèle de stockage réel des données XML.</span><span class="sxs-lookup"><span data-stu-id="6349a-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="6349a-602">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="6349a-603">Formats de fichiers image</span><span class="sxs-lookup"><span data-stu-id="6349a-603">Picture file formats</span></span>

<span data-ttu-id="6349a-604">Dans le contexte de cette proposition, les données externes sont invariablement une image bitmap ou un fichier qui est utilisé pour produire une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="6349a-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="6349a-605">Au niveau de rendu 0, aucun format de bitmap externe ne doit être pris en charge--les chemins d’accès peuvent uniquement être remplis avec des couleurs unies.</span><span class="sxs-lookup"><span data-stu-id="6349a-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="6349a-606">Pour afficher l’ensemble complet des remplissages de niveau 1, les bitmaps doivent être prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6349a-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="6349a-607">Le niveau de rendu 1 comprend (uniquement) les formats suivants :</span><span class="sxs-lookup"><span data-stu-id="6349a-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="6349a-608">JFIF, c’est-à-dire les données de format ISO/IEC 10918 incorporées dans un fichier avec l’en-tête JFIF (qui peut être considéré comme un marqueur APP0 particulier après le fabricant SOI-ci) et incluant (uniquement) la plage de formats JPEG prise en charge par le code IJG V6.</span><span class="sxs-lookup"><span data-stu-id="6349a-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="6349a-609">PNG, tel que défini par la spécification PNG version 1,0.</span><span class="sxs-lookup"><span data-stu-id="6349a-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="6349a-610">Le niveau de rendu 2 prend également en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6349a-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="6349a-611">GIF, tel que défini par la spécification GIF publiée par CompuServ dans 1987 (généralement appelé « GIF87a »).</span><span class="sxs-lookup"><span data-stu-id="6349a-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="6349a-612">GIF89a doit également être pris en charge à ce niveau, en fonction de la restriction selon laquelle les données ne doivent pas contenir de blocs d’extension nécessitant une interprétation pour afficher la bitmap autre que Graphics Control extensionswithouta requirement pour l’entrée utilisateur ou un délai.</span><span class="sxs-lookup"><span data-stu-id="6349a-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="6349a-613">Cela permet d’inclure des commentaires, mais pas l’extension de texte brut.</span><span class="sxs-lookup"><span data-stu-id="6349a-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="6349a-614">Une application peut insérer des extensions d’application (0x21, 0xFF) mais, à l’aide de la terminologie de cette proposition, celles-ci ne doivent contenir que des données de modification, et non de rendu.</span><span class="sxs-lookup"><span data-stu-id="6349a-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="6349a-615">Tout autre format de données utilisé dans le graphique force ce graphique à avoir au moins un niveau de modification 3 et éventuellement un niveau de rendu 3 (si les données sont nécessaires pour effectuer le rendu du graphique).</span><span class="sxs-lookup"><span data-stu-id="6349a-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="6349a-616">Une application est encouragée à publier les formats qu’elle prend en charge.</span><span class="sxs-lookup"><span data-stu-id="6349a-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="6349a-617">Par exemple, Microsoft Office prend en charge les formats supplémentaires suivants en mode natif et peut donc écrire des données de modification dans ce formulaire :</span><span class="sxs-lookup"><span data-stu-id="6349a-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="6349a-618">WMF--Windows Metafile (format Win 3,1)</span><span class="sxs-lookup"><span data-stu-id="6349a-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="6349a-619">EMF--Windows « Enhanced » Metafile (format Win32)</span><span class="sxs-lookup"><span data-stu-id="6349a-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="6349a-620">PICT--Mac OS fichier. QuickDraw PICT (toutes les versions, mais sans enregistrements QuickTime ou autres extensions)</span><span class="sxs-lookup"><span data-stu-id="6349a-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="6349a-621">BMP--format de fichier bitmap Windows, formats « OS/2 » (BITMAPCORE), BITMAPINFO,, BITMAPV4 et BITMAPV5</span><span class="sxs-lookup"><span data-stu-id="6349a-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="6349a-622">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="6349a-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="6349a-623">vecteur</span><span class="sxs-lookup"><span data-stu-id="6349a-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="6349a-624">Un tracé graphique vectoriel est encodé en tant que PCDATA.</span><span class="sxs-lookup"><span data-stu-id="6349a-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="6349a-625">Le contenu de l’élément v est mélangé, contenant une description du chemin d’accès du vecteur éventuellement paramétrable avec des éléments p.</span><span class="sxs-lookup"><span data-stu-id="6349a-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="6349a-626">Retour à la vue d’ensemble du VML</span><span class="sxs-lookup"><span data-stu-id="6349a-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

