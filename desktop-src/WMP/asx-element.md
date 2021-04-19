---
title: Élément ASX
description: L’élément ASX définit un fichier en tant que métafichier.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Élément ASX lecteur Windows Media
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521679"
---
# <a name="asx-element"></a>Élément ASX

L’élément **ASX** définit un fichier en tant que métafichier.

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>Attributs

`VERSION` (requis)

Nombre décimal représentant le numéro de version de la syntaxe pour le métafichier. Défini sur 3 ou 3,0.

**PREVIEWMODE** (facultatif)

Valeur indiquant si le lecteur Windows Media passe en mode aperçu avant de lancer le premier clip.

Doit avoir l’une des valeurs suivantes.



| Valeur | Description                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Le lecteur Windows Media passe en mode aperçu avant de visionner le premier clip.                            |
| Non    | Valeur par défaut. Le lecteur Windows Media n’entre pas en mode aperçu avant de commencer le premier clip. |



 

**BANNERBAR** (facultatif)

Valeur indiquant si le lecteur Windows Media réserve de l’espace pour un graphique de bannière.

Doit avoir l’une des valeurs suivantes.



| Valeur | Description                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Valeur par défaut. Le lecteur Windows Media réserve de l’espace pour la barre de bannière uniquement lorsqu’un élément de contenu en contient un.                       |
| FIXED | Le lecteur Windows Media réserve un espace fixe pour un graphique de bannière pour chaque morceau de contenu lu, qu’il y ait une bannière associée. |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents | Aucun L’élément **ASX** doit être le premier élément de chaque métafichier.                                                                                                 |
| Éléments enfants  | **abstract**, **Author**, **Banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **moreinfo**, **PREVIEWDURATION**, **param**, **REPEAT**, **title** |



 

## <a name="remarks"></a>Notes

Les quatre premiers caractères d’une sélection de métafichiers doivent être « <ASX ». Les autres éléments définis dans l’étendue de l’élément **ASX** , tels que **title** et **Author**, sont associés aux informations affichées par le lecteur Windows Media.

Pour le lecteur Windows Media, le numéro de version de la syntaxe est 3,0. Le lecteur Windows Media prend en charge toutes les versions précédentes de la syntaxe Metafile. Les valeurs acceptables pour l’attribut **version** incluent à la fois 3,0 et 3 (sans virgule décimale).

Si la valeur de l’attribut **PREVIEWMODE** est Yes, le lecteur Windows Media passe immédiatement en mode aperçu avant de lancer le premier clip. Lorsque le lecteur Windows Media passe en mode aperçu, il affiche un aperçu de chaque clip référencé dans le métafichier. L’élément **PREVIEWDURATION** détermine la durée de chaque aperçu.

L’attribut **BANNERBAR** définit si le lecteur Windows Media réserve de l’espace pour un graphique de bannière. Une bannière est un graphique qui s’affiche dans la zone d’affichage vidéo pendant la diffusion du contenu multimédia. (Utilisez l’élément **bannière** pour ajouter une bannière au contenu.) Si la valeur de **BANNERBAR** est fixe, le lecteur Windows Media réserve de l’espace de bannière pour chaque contenu multimédia, que le contenu du média ait une bannière. Si un contenu multimédia n’est associé à aucune bannière, l’espace réservé pour celui-ci est noir. Si la valeur de l’attribut **BANNERBAR** est auto, le lecteur Windows Media réserve de l’espace pour la bannière uniquement lorsque le contenu multimédia en contient un.

Si vous créez un métafichier avec plusieurs clips (éléments **entry** ou **ENTRYREF** ) et que vous définissez la valeur de l’attribut **BANNERBAR** sur auto, le lecteur Windows Media peut se redimensionner pour permettre l’espace pour un graphique de bannière pour un clip, puis le redimensionner si le clip suivant ne contient pas de graphique de bannière. Si vous souhaitez que la taille de la fenêtre reste la même (sauf en cas de modification de la taille de la vidéo), utilisez la valeur fixe de l’attribut **BANNERBAR** .

L’espace réservé pour un graphique de bannière est de 32 pixels de haut en 194 pixels de large. L’espace réservé apparaît en dessous du contenu vidéo rendu et de 6 pixels au-dessus du bord inférieur de la zone vidéo, ce qui permet d’obtenir de l’espace pour la bordure de la zone vidéo de 6 pixels. L’espace de bannière réservé est centré horizontalement.

Le lecteur Windows Media effectue le rendu du graphique à partir du pixel le plus à gauche de l’espace de la bannière. Si le graphique remplit la totalité de l’espace, il s’affiche centré horizontalement. Dans le cas contraire, il y aura un espace de fin. Notez que la largeur minimale du lecteur Windows Media est toujours plus large que la taille du clip vidéo, quelle que soit la valeur de l’attribut **BANNERBAR** .

## <a name="examples"></a>Exemples


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 70 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





