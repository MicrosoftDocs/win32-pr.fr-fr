---
title: Élément BANNER
description: L’élément BANNER définit une URL vers un fichier graphique qui s’affiche dans le panneau d’affichage.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Élément de bannière lecteur Windows Media
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543873"
---
# <a name="banner-element"></a>Élément BANNER

L’élément **Banner** définit une URL vers un fichier graphique qui s’affiche dans le panneau d’affichage.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Attributs

**Href** (obligatoire)

URL d’un fichier graphique affiché dans le panneau d’affichage.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                   |
|-----------------|----------------------------|
| Éléments parents | **ASX**, **entrée**         |
| Éléments enfants  | **abstract**, **moreinfo** |



 

## <a name="remarks"></a>Notes

Cet élément définit une URL vers un fichier graphique qui s’affiche dans le panneau d’affichage du lecteur Windows Media, sous le contenu de la vidéo. Si le support est uniquement audio, le graphique de bannière s’affiche de lui-même. Le lecteur Windows Media réserve un espace de 32 pixels de haut en 194 pixels de large (la barre de bannière) du graphique. Si le graphique défini dans l’URL est plus petit, il s’affiche à sa taille d’origine. Si le graphique est plus grand que l’espace réservé, le lecteur Windows Media rogne l’image pour l’ajuster à l’espace.

Vous pouvez utiliser un élément **abstrait** dans la portée de l’élément **bannière** pour afficher du texte sous la forme d’une info-bulle lorsque l’utilisateur place le pointeur de la souris sur le graphique de la bannière. Un élément **moreinfo** dans un élément **Banner** définit une URL vers laquelle l’utilisateur est tenu quand l’utilisateur clique sur le graphique de bannière. (L’URL peut être n’importe quel chemin d’accès ou protocole, tel qu’un lien de messagerie électronique, une URL HTTP (Hypertext Transfer Protocol) vers un site Web ou même une commande Microsoft JScript.) Lorsque le pointeur est déplacé au-dessus du graphique, le graphique est gaufré et ressemble à un bouton.

Un élément de **bannière** défini pour un élément **ASX** s’affiche pendant la lecture de tous les clips de la playlist. Un élément **Banner** défini dans un élément **entry** s’affiche uniquement lors de la diffusion de ce clip et, pendant cette période, remplace les bannières définies dans l’élément **ASX** parent. Vous pouvez spécifier la façon dont le lecteur Windows Media réserve de l’espace pour la bannière en définissant l’attribut **BANNERBAR** de l’élément **ASX** .

Les images de bannière ne sont pas prises en charge avec les fichiers DRM ou lorsque le lecteur Windows Media est incorporé dans une page Web.

## <a name="examples"></a>Exemples

Voici un exemple d’élément **Banner** sans éléments enfants :


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



Voici un exemple d’élément **Banner** contenant des éléments **abstract** et **moreinfo** .


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





