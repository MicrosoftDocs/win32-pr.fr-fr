---
title: W (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- windows
- alignée sur la fenêtre
- coordonnées de la fenêtre
- Wireframe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013969"
---
# <a name="w-opengl"></a>W (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**fenetre**
</dt> <dd>

Sous-région du trame, généralement rectangulaire, dont les pixels ont tous la même configuration de mémoire tampon. Un contexte OpenGL est restitué dans une fenêtre à la fois.

</dd> <dt>

<span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**alignée sur la fenêtre**
</dt> <dd>

Lorsque vous faites référence à des segments de ligne ou à des arêtes de polygones, implique qu’ils sont parallèles aux limites de la fenêtre. (Dans OpenGL, la fenêtre est rectangulaire, avec des bords horizontaux et verticaux). Lorsque vous faites référence à un modèle de polygone, implique que le modèle est fixe par rapport à l’origine de la fenêtre.

</dd> <dt>

<span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**coordonnées de la fenêtre**
</dt> <dd>

Système de coordonnées d’une fenêtre. Il est important de faire la distinction entre les noms des pixels, qui sont discrets et le système de coordonnées de la fenêtre, qui est continu. Par exemple, le pixel situé dans le coin inférieur gauche d’une fenêtre est pixel (0,0); les coordonnées de la fenêtre du centre de ce pixel sont (0,5, 0,5, z). Notez que les coordonnées des fenêtres incluent une profondeur, ou z, un composant et que ce composant est également continu.

</dd> <dt>

<span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**Wireframe**
</dt> <dd>

Représentation d’un objet qui contient uniquement des segments de ligne. En règle générale, les segments de ligne indiquent les bords de polygone.

</dd> </dl>

 

 




