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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011496"
---
# <a name="glpushattrib-function"></a>glPushAttrib fonction)

Exécute un push de la pile d’attributs.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mask* 
</dt> <dd>

Masque qui indique les attributs à enregistrer. Les constantes de masque symbolique et leur état OpenGL associé sont les suivantes (la liste des paragraphes en retrait répertorie les attributs qui sont enregistrés) :

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_bit de tampon amort \_ \_ 
</dt> <dd>

Valeur effacée de la mémoire tampon d’accumulation

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit de \_ mémoire tampon de couleur GL \_
</dt> <dd>

\_Bit d’activation du test du GL alpha \_

Fonction de test alpha et valeur de référence

Bit d’activation de la \_ fusion GL

Fusion des fonctions source et de destination

\_Bit d’activation du tramage GL

\_Paramètre de \_ mémoire tampon de dessin GL

\_Bit logique d’activation du GL \_

Fonction Logic op

Valeurs claires en mode couleur et en mode index

Writemasks en mode couleur et en mode index

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_bit actuel du GL \_
</dt> <dd>

Couleur RVBA actuelle

Index des couleurs actuelles

Vecteur normal actuel

Coordonnées de texture actuelles

Position raster actuelle indicateur de \_ la \_ position raster \_ actuelle de la position raster \_

Couleur RVBA associée à la position de la trame actuelle

Index de couleurs associé à la position de la trame actuelle

Coordonnées de texture associées à la position de trame actuelle

Indicateur de l’indicateur de périphérie du GL \_ \_

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_bit de \_ mémoire tampon de profondeur GL \_
</dt> <dd>

\_Bit d’activation du test de profondeur du GL \_

Fonction de test de la mémoire tampon de profondeur

Valeur effacée de la mémoire tampon de profondeur

Profondeur du GL \_ \_ WRITEMASK activer le bit

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit d’activation du GL \_
</dt> <dd>

Indicateur de test de comptabilité \_ alpha \_

\_Indicateur de \_ normalisation automatique du GL

Indicateur de fusion du GL \_

Activer le service bits pour les plans de découpage définissables par l’utilisateur

\_matériau de couleur GL \_

Indicateur de visage de \_ CULLING GL \_

Indicateur de test de \_ profondeur du GL \_

\_Indicateur de tramage GL

\_Indicateur de brouillard GL

GL \_ clair *i* où 0 <= *i* < des \_ lumières du GL Max \_

\_Indicateur d’éclairage GL

Indicateur de lissage de \_ ligne GL \_

\_ \_ Indicateur STIPPLE de la ligne GL

Indicateur de logique de l' \_ op GL couleur \_ \_

\_Indicateur d' \_ op logique d’index GL \_

GL \_ Map1 \_ x où x est un type de carte

GL \_ map2 \_ x où x est un type de carte

\_Indicateur de normalisation GL

Indicateur de lissage du \_ point GL \_

\_Indicateur de \_ ligne de décalage du polygone GL \_

\_Indicateur de \_ remplissage de décalage de polygone GL \_

\_Indicateur de \_ point de décalage de polygone GL \_

\_Indicateur de lissage de polygones GL \_

\_Indicateur de STIPPLE de polygones GL \_

Indicateur de test de \_ ciseaux du GL \_

Indicateur de test de \_ stencil du GL \_

\_ \_ Indicateur 1D de la texture GL

\_Indicateur de texture GL \_ 2D

Flags GL \_ texture \_ GEN \_ x où x est S, T, R ou Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>\_bit d’évaluation du GL \_
</dt> <dd>

GL \_ Map1 \_ x active bits, où x est un type de carte

GL \_ map2 \_ x active bits, où x est un type de carte

points de terminaison de grille 1D et divisions

points de terminaison de grille 2D et divisions

Bit d’activation de la \_ normalisation automatique du GL \_

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit de brouillard GL \_
</dt> <dd>

\_Indicateur d’activation du brouillard GL

Couleur de brouillard

Densité de brouillard

Démarrage du brouillard linéaire

Fin du brouillard linéaire

Index de brouillard

Valeur du mode de \_ brouillard GL \_

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit indicateur \_ GL
</dt> <dd>

Paramètre de l’indicateur de correction de la \_ perspective GL \_ \_

\_Paramètre d' \_ indicateur d’arrondi de point GL \_

\_Paramètre d' \_ indicateur de lissage de ligne GL \_

\_Paramètre d' \_ indicateur de lissage de polygones GL \_

Paramètre de l' \_ indicateur de brouillard GL \_

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit d’éclairage GL \_
</dt> <dd>

Bit de couleur GL- \_ \_ activer le bit

\_Valeur de \_ face du matériau de couleur GL \_

Paramètres de matériau de couleur qui effectuent le suivi de la couleur actuelle

Couleur de scène ambiante

\_Valeur de \_ la \_ visionneuse locale du modèle de lumière GL \_

\_Paramètre côté « GL Light \_ Model \_ deux \_ côtés »

Bit d’activation de l' \_ éclairage GL

Activer le bit pour chaque lumière

Intensité ambiante, diffuse et spéculaire pour chaque lumière

Orientation, position, exposant et angle de coupure pour chaque lumière

Facteurs d’atténuation constante, linéaire et quadratique pour chaque lumière

Couleur ambiante, diffuse, spéculaire et émissif pour chaque matière

Index de couleurs ambiants, diffuses et spéculaires pour chaque matériau

Exposant spéculaire pour chaque paramètre de modèle d' \_ ombrage de la comptabilité matières \_

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit de ligne GL \_ 
</dt> <dd>

Indicateur de lissage de \_ ligne GL \_

Bit de STIPPLE de ligne GL- \_ \_ activer

Modèle de stipple de ligne et compteur de répétition

Largeur de ligne

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit de liste GL \_
</dt> <dd>

Paramètre de base de la \_ liste GL \_

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit du \_ mode de pixel GL \_
</dt> <dd>

\_ \_ Paramètres de décalage rouge et \_ de \_ balance rouge du GL

\_ \_ Valeurs de l’échelle vert GL et de l' \_ échelle verte GL \_

\_Décalage bleu GL \_ et \_ échelle bleue \_ GL

\_Décalage alpha du GL \_ et échelle du GL \_ alpha \_

\_ \_ Décalage de profondeur GL et \_ échelle de profondeur GL \_

Décalage de l’index GL \_ \_ et valeurs de décalage de l' \_ index GL \_

\_Couleurs de la carte GL \_ et indicateurs de stencil de la \_ carte GL \_

\_Zooms GL \_ X et \_ Zoom GL \_ Y

Paramètre de tampon de \_ lecture GL \_

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit de point GL \_
</dt> <dd>

Indicateur de lissage du \_ point GL \_

Taille du point

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit de polygone GL \_
</dt> <dd>

Bit d’activation de la face de l' \_ élimination GL \_

\_Valeur du \_ mode visage d’élimination du GL \_

\_Indicateur de \_ face avant GL

\_Paramètre du \_ mode polygone GL

\_Indicateur de lissage de polygones GL \_

STIPPLE de l’activation du polygone de GL \_ \_

\_Indicateur de \_ remplissage de décalage de polygone GL \_

\_Indicateur de \_ ligne de décalage du polygone GL \_

\_Indicateur de \_ point de décalage de polygone GL \_

\_facteur de \_ décalage du polygone GL \_

\_unités de décalage de polygones GL \_ \_

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_STIPPLE- \_ \_ bit de polygone de GL
</dt> <dd>

Image Polygon stipple

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_bit de ciseaux de GL \_
</dt> <dd>

Indicateur de test de \_ ciseaux du GL \_

Zone de ciseaux

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_bit de \_ tampon de stencil du GL \_
</dt> <dd>

\_Bit d’activation du test du gabarit GL \_

Fonction de stencil et valeur de référence

Masque de valeur de stencil

Actions de réussite de la passe de tampon d’échec, de réussite et de profondeur du stencil

Valeur Clear de la mémoire tampon du stencil

Tampon de stencil writemask

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit de texture GL \_
</dt> <dd>

Activer bits pour les quatre coordonnées de texture

Couleur de la bordure pour chaque image de texture

Fonction minimisation pour chaque image de texture

Fonction d’agrandissement pour chaque image de texture

Coordonnées de texture et mode habillage pour chaque image de texture

Couleur et mode pour chaque environnement de texture

Activer bits GL \_ texture \_ GEN \_ *x*; *x* est S, T, R et Q

\_ \_ \_ Paramètre du mode de la génération de texture GL pour S, T, R et Q

équations de plan glTexGen pour S, T, R et Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit de transformation GL \_
</dt> <dd>

Coefficients des six plans de découpage

Activer le service bits pour les plans de découpage définissables par l’utilisateur

Valeur du mode de \_ matrice GL \_

\_Indicateur de normalisation GL

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit de fenêtre d’affichage GL \_
</dt> <dd>

Plage de profondeur (proche et loin)

Origine de la fenêtre d’affichage et étendue

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**dépassement de capacité de la \_ pile GL \_**</dt> </dl>    | La fonction a été appelée alors que la pile d’attributs était pleine.<br/>                                                                |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **glPushAttrib** prend un argument, un masque qui indique les groupes de variables d’État à enregistrer sur la pile d’attributs. Les constantes symboliques sont utilisées pour définir des bits dans le masque. Le paramètre Mask est généralement construit en appliquant l’opération **or** logique à plusieurs de ces constantes. Vous pouvez utiliser le masque spécial GL \_ tous \_ les \_ bits d’attrib pour enregistrer tous les États empilables.

La fonction [**glPopAttrib**](glpopattrib.md) restaure les valeurs des variables d’état enregistrées avec la dernière commande **glPushAttrib** . Ceux qui ne sont pas enregistrés restent inchangés.

C’est une erreur de transmettre des attributs à une pile complète, ou d’afficher des attributs sur une pile vide. Dans les deux cas, l’indicateur d’erreur est défini et aucune autre modification n’est apportée à l’État OpenGL.

Initialement, la pile d’attributs est vide.

Toutes les valeurs de l’État OpenGL ne peuvent pas être enregistrées dans la pile d’attributs. Par exemple, vous ne pouvez pas enregistrer l’état du Pack de pixels et décompresser, l’état du mode de rendu et l’état de sélection et de commentaires.

La profondeur de la pile d’attributs dépend de l’implémentation, mais elle doit être au moins égale à 16.

Les fonctions suivantes récupèrent les informations relatives à **glPushAttrib** et [**glPopAttrib**](glpopattrib.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec argument la \_ profondeur de la pile GL attrib \_ \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument GL max. profondeur de la \_ \_ \_ pile \_

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





