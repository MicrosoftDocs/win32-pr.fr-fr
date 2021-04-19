---
title: F (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- visages
- ombrage plat
- brouillard
- polices
- fragments
- framebuffers
- face avant
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509695"
---
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**se**
</dt> <dd>

Un côté d’un polygone. Chaque polygone a deux visages : une face avant et une face arrière. Une seule face est toujours visible dans la fenêtre. La visibilité de la face arrière ou de l’avant est déterminée une fois que le polygone est projeté dans la fenêtre. Après cette projection, si les bords du polygone sont dirigés dans le sens des aiguilles d’une montre, l’une des faces est visible. s’il est dirigé vers le sens inverse des aiguilles d’une représente, l’autre visage est visible. Que le sens horaire corresponde à l’avant ou à l’arrière (et dans le sens inverse, à l’arrière ou à l’avant) est déterminé par le programmeur OpenGL.

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**ombrage plat**
</dt> <dd>

Fait référence à la coloration d’une primitive avec une couleur constante unique dans son étendue, plutôt que de lisser l’interpolation des couleurs sur l’ensemble de la primitive. Consultez l' [Ombrage Gouraud](g.md).

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**vont**
</dt> <dd>

Technique de rendu qui peut être utilisée pour simuler des effets atmosphériques, tels que le trouble, le brouillard et les smog en confondant les couleurs des objets sur une couleur d’arrière-plan en fonction de la distance par rapport à la visionneuse. Le brouillard facilite également la perception de la distance par rapport à la visionneuse, en donnant un repère de profondeur. Voir aussi [profondeur-cueing](d.md).

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**son**
</dt> <dd>

Groupe de représentations de caractères graphiques généralement utilisé pour afficher des chaînes de texte. Les caractères peuvent être des lettres latines, des symboles mathématiques, des idéogrammes asiatiques, des Hieroglyphs égyptiennes, etc.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**échantillon**
</dt> <dd>

Données graphiques générées par la pixellisation des primitives. Chaque fragment correspond à un pixel unique et comprend des valeurs de couleur, de profondeur et parfois de coordonnées de texture.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**trame**
</dt> <dd>

Pile de bitplanes. Toutes les mémoires tampons d’une fenêtre ou d’un contexte donnés. Comprend parfois la mémoire en pixels de l’accélérateur matériel Graphics. Voir aussi [Bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**face avant**
</dt> <dd>

Consultez la section face.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**
</dt> <dd>

Le volume de la vue déformé par la Division de perspective.

</dd> </dl>

 

 




