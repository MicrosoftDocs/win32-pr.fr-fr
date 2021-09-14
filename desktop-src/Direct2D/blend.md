---
title: 'Effet de fusion :'
description: Utilisez l’effet de fusion pour combiner 2 images. Cet effet a 26 modes de fusion.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- effet de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853043123c6eea9a87656a7450b1295236ed5d6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114194"
---
# <a name="blend-effect"></a>Effet de fusion :

Utilisez l’effet de fusion pour combiner 2 images. Cet effet a 26 modes de fusion.

Le CLSID de cet effet est CLSID \_ D2D1Blend.

-   [Exemples de fusion](#blending-examples)
-   [Propriétés d’effet](#effect-properties)
-   [Modes de fusion](#blend-modes)
-   [Conversions de l’espace colorimétrique TSL](#hsl-color-space-conversions)
    -   [Conversion de RVB en TSL](#converting-from-rgb-to-hsl)
    -   [Conversion de TSL en RGB](#converting-from-hsl-to-rgb)
-   [Bitmap de sortie](#output-bitmap)
-   [Exemple de code](#sample-code)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="blending-examples"></a>Exemples de fusion

Voici un exemple d’image de chaque mode de fusion de l’effet de fusion. La section suivante présente une liste complète des modes de fusion et des propriétés de mode correspondantes.

![exemple de capture d’écran de tous les modes de fusion disponibles.](images/blend-modes.png)

Voici un autre exemple utilisant le mode d’exclusion.



| Avant image 1                                                             |
|----------------------------------------------------------------------------|
| ![première image source avant l’effet.](images/default-before.jpg)    |
| Avant image 2                                                             |
| ![deuxième image avant l’effet.](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![image après la transformation.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                 | Description                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> \_Mode d2d1 Blend \_ prop \_<br/> | Mode de fondu utilisé pour l’effet. Pour plus d’informations, consultez [modes de fusion](#blend-modes) . Le type est D2D1 \_ Blend \_ mode.<br/> La valeur par défaut est D2D1 \_ Blend \_ mode \_ Multiply.<br/> |



 

## <a name="blend-modes"></a>Modes de fusion

Le tableau ci-dessous montre tous les modes de fusion de cet effet. Les fonctions d’assistance nécessaires pour calculer la sortie de l’effet se trouvent dans la section suivante.

Couleur : O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, b <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub></sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + B <sub>RGB</sub> \* b <sub>a</sub> \* (1-f <sub>a</sub>)

Alpha : O<sub>a</sub> = F<sub>a</sub> \* (1-B<sub>a</sub>) + B<sub>a</sub>

Où :

-   O<sub>PRGB</sub> est la couleur de sortie prémultipliée
-   O<sub>a est une</sub> sortie alpha
-   B<sub>RVB</sub> est la couleur de destination non prémultipliée
-   B<sub>a est une</sub> destination alpha
-   F<sub>RGB</sub> est la couleur source non prémultipliée
-   F<sub>a est une</sub> source alpha
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) est une fonction de fusion qui varie en mode par fusion

Certains modes de fusion nécessitent une conversion vers et à partir de l’espace de couleurs teinte, saturation, luminosité (TSL) sur RVB.




| Énumération | Sommaire | 
|-------------|----------|
| D2D1_BLEND_MODE_DARKEN | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /> | 
| D2D1_BLEND_MODE_MULTIPLY | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /> | 
| D2D1_BLEND_MODE_COLOR_BURN | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /> | 
| D2D1_BLEND_MODE_LINEAR_BURN | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /> | 
| D2D1_BLEND_MODE_DARKER_COLOR | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /> | 
| D2D1_BLEND_MODE_LIGHTEN | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /> | 
| D2D1_BLEND_MODE_SCREEN | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /> | 
| D2D1_BLEND_MODE_COLOR_DODGE | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /> | 
| D2D1_BLEND_MODE_LINEAR_DODGE | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /> | 
| D2D1_BLEND_MODE_LIGHTER_COLOR | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /> | 
| D2D1_BLEND_MODE_OVERLAY | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /> | 
| D2D1_BLEND_MODE_SOFT_LIGHT | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /> | 
| D2D1_BLEND_MODE_HARD_LIGHT | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /> | 
| D2D1_BLEND_MODE_VIVID_LIGHT | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /> | 
| D2D1_BLEND_MODE_LINEAR_LIGHT | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /> | 
| D2D1_BLEND_MODE_PIN_LIGHT | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /> | 
| D2D1_BLEND_MODE_HARD_MIX | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /> | 
| D2D1_BLEND_MODE_DIFFERENCE | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> -b<sub>RGB</sub>) | 
| D2D1_BLEND_MODE_EXCLUSION | Formules de fusion de base avec <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>)<sub>= F</sub> <sub>RGB</sub> + b<sub>RGB 2 * f RVB *</sub> b<sub>RGB</sub> | 
| D2D1_BLEND_MODE_HUE | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /> | 
| D2D1_BLEND_MODE_SATURATION | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /> | 
| D2D1_BLEND_MODE_COLOR | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /> | 
| D2D1_BLEND_MODE_LUMINOSITY | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /> | 
| D2D1_BLEND_MODE_DISSOLVE | Soit :<ul><li>Une scène en coordonnées XY pour le pixel actuel</li><li>Un générateur de nombres pseudo-aléatoires déterministe (XY) basé sur la coordonnée de valeur de départ XY, avec une distribution sans biais de valeurs de [0, 1]</li></ul><br /><img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br /> | 
| D2D1_BLEND_MODE_SUBTRACT | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /> | 
| D2D1_BLEND_MODE_DIVISION | Formule de fusion de base pour Alpha uniquement. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /> | 




 

> [!Note]  
> Pour tous les modes de fusion, la valeur de sortie est prémultipliée et ancrée à la plage \[ 0, 1 \] .

 

## <a name="hsl-color-space-conversions"></a>Conversions de l’espace colorimétrique TSL

Le composant luminosité est calculé à l’aide des pondérations RVB ici :

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Conversion de RVB en TSL

![formule mathématique décrivant la transformation de la couleur RVB à la couleur TSL.](images/blend-rgb-to-hsl-1.png)

Cela place *S* et *L* dans la plage \[ 0,0, 1,0 \] et *H* dans la plage \[ -1,0, 5,0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Conversion de TSL en RGB

Pour convertir d’une autre façon, nous utilisons l’inverse des calculs précédents.

Si *S* = 0, alors *R*  =  *G*  =  *B*  =  *L*

Dans le cas contraire, il existe six cas dépendants de la teinte :

Si *H* est supérieur à 0, les valeurs se trouvent dans le secteur rouge/Magenta où *R*  >  *B*  >  *G*.

![equaiton : étape 1 de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1rm.png)

Si *H* est supérieur ou égal à 0 et inférieur à 1, les valeurs se trouvent dans le secteur rouge/jaune où *R*  >  *G*  >  *B*.

![mathématiques equaiton étape deux de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1ry.png)

Si *H* est supérieur ou égal à 1 et inférieur à 2, les valeurs se trouvent dans le secteur jaune/vert où *G*  >  *R*  >  *B*.

![mathématiques equaiton étape trois de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1yg.png)

Si *H* est supérieur ou égal à 2 et inférieur à 3, les valeurs se trouvent dans le secteur vert/cyan où *G*  >  *B*  >  *R*.

![mathématiques equaiton étape quatre de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1gc.png)

Si *H* est supérieur ou égal à 3 et inférieur à 4, les valeurs se trouvent dans le secteur cyan/bleu, où *B*  >  *G*  >  *R*.

![mathématiques equaiton étape 5 de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1cb.png)

Si *H* est supérieur ou égal à 4, les valeurs se trouvent dans le secteur bleu/magenta où *B*  >  *R*  >  *G*.

![mathématiques equaiton étape six de six convertissant la couleur TSL en RVB.](images/blend-hsl-to-rgb-1bm.png)

Étant donné que les modes de fusion apportent des combinaisons arbitraires de composants TSL à partir de deux couleurs différentes, il est courant que la valeur RVB convertie soit hors de la gamme, c’est-à-dire qu’un ou plusieurs composants de canal soient en dehors de la plage légale \[ 0,0, 1,0 \] . Ces couleurs sont remises en gamme en réduisant au minimum la saturation, tout en préservant la teinte et la luminosité :

![formule mathématique décrivant les corrections requises pour les instances de non-gamme.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Bitmap de sortie

Le bitmap de sortie de cet effet est toujours la taille de l’Union des deux images d’entrée.

## <a name="sample-code"></a>Exemple de code

Pour obtenir un exemple de cet effet, téléchargez l' [exemple de modes d’effet composite de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

