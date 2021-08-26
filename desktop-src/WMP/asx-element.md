---
title: Élément ASX
description: L’élément ASX définit un fichier en tant que métafichier.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- élément ASX Lecteur Windows Media
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 509cdbc25c57c6d0b556433c3bee8b1e68083248c8356769a31529b83c2df1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902828"
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

valeur indiquant si Lecteur Windows Media passe en mode aperçu avant de relire le premier clip.

Il doit s’agir de l’une des valeurs suivantes.



| Valeur | Description                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Lecteur Windows Media passe en mode aperçu avant de lancer le premier clip.                            |
| Non    | Valeur par défaut. Lecteur Windows Media n’entre pas en mode aperçu avant de visionner le premier clip. |



 

**BANNERBAR** (facultatif)

valeur indiquant si Lecteur Windows Media réserve de l’espace pour un graphique de bannière.

Il doit s’agir de l’une des valeurs suivantes.



| Valeur | Description                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Valeur par défaut. Lecteur Windows Media réserve de l’espace pour la barre de bannière uniquement lorsqu’un élément de contenu en contient un.                       |
| FIXED | Lecteur Windows Media réserve un espace fixe pour un graphique de bannière pour chaque morceau de contenu joué, qu’il existe une bannière associée. |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents | Aucun. L’élément **ASX** doit être le premier élément de chaque métafichier.                                                                                                 |
| Éléments enfants  | **abstract**, **Author**, **Banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **moreinfo**, **PREVIEWDURATION**, **param**, **REPEAT**, **title** |



 

## <a name="remarks"></a>Remarques

Les quatre premiers caractères d’une sélection de métafichiers doivent être « <ASX ». les autres éléments définis dans l’étendue de l’élément **ASX** , tels que **TITLE** et **AUTHOR**, sont associés aux informations affichées par Lecteur Windows Media.

pour Lecteur Windows Media, le numéro de version de la syntaxe est 3,0. Lecteur Windows Media prend en charge toutes les versions précédentes de la syntaxe metafile. Les valeurs acceptables pour l’attribut **version** incluent à la fois 3,0 et 3 (sans virgule décimale).

si la valeur de l’attribut **PREVIEWMODE** est YES, Lecteur Windows Media passe immédiatement en mode aperçu avant de lancer le premier clip. lorsque Lecteur Windows Media passe en mode aperçu, il affiche chaque clip référencé dans le métafichier. L’élément **PREVIEWDURATION** détermine la durée de chaque aperçu.

l’attribut **BANNERBAR** définit si Lecteur Windows Media réserve de l’espace pour un graphique de bannière. Une bannière est un graphique qui s’affiche dans la zone d’affichage vidéo pendant la diffusion du contenu multimédia. (Utilisez l’élément **bannière** pour ajouter une bannière au contenu.) si la valeur de **BANNERBAR** est fixe, Lecteur Windows Media réserve de l’espace de bannière pour chaque morceau de contenu multimédia, que le contenu du média ait une bannière. Si un contenu multimédia n’est associé à aucune bannière, l’espace réservé pour celui-ci est noir. si la valeur de l’attribut **BANNERBAR** est AUTO, Lecteur Windows Media réserve de l’espace pour la bannière uniquement lorsque le contenu multimédia en contient un.

si vous créez un métafichier avec plusieurs clips (éléments **entry** ou **ENTRYREF** ) et définissez la valeur de l’attribut **BANNERBAR** sur AUTO, Lecteur Windows Media peut se redimensionner pour permettre l’espace pour un graphique de bannière pour un clip, puis redimensionner à nouveau si le clip suivant ne contient pas de graphique de bannière. Si vous souhaitez que la taille de la fenêtre reste la même (sauf en cas de modification de la taille de la vidéo), utilisez la valeur fixe de l’attribut **BANNERBAR** .

L’espace réservé pour un graphique de bannière est de 32 pixels de haut en 194 pixels de large. L’espace réservé apparaît en dessous du contenu vidéo rendu et de 6 pixels au-dessus du bord inférieur de la zone vidéo, ce qui permet d’obtenir de l’espace pour la bordure de la zone vidéo de 6 pixels. L’espace de bannière réservé est centré horizontalement.

Lecteur Windows Media effectue le rendu du graphique à partir du pixel le plus à gauche de l’espace de la bannière. Si le graphique remplit la totalité de l’espace, il s’affiche centré horizontalement. Dans le cas contraire, il y aura un espace de fin. notez que la largeur minimale de Lecteur Windows Media est toujours plus large que la taille du clip vidéo, quelle que soit la valeur de l’attribut **BANNERBAR** .

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

[**Windows Informations de référence sur les éléments de métafichier multimédia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Référence du métafichier multimédia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





