---
title: D (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- profondeur cueing
- afficher les listes
- tramage
- doubles tampons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739500"
---
# <a name="d-opengl"></a>D (OpenGL)

[A](a.md) [B](b.md) [C](c.md) D [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**profondeur**
</dt> <dd>

Fait généralement référence à la coordonnée de la fenêtre z.

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**profondeur cueing**
</dt> <dd>

Technique de rendu qui assigne une couleur en fonction de la distance par rapport au point de vue.

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**afficher la liste**
</dt> <dd>

Liste nommée de commandes OpenGL. Les listes d’affichage étant toujours stockées sur le serveur, vous pouvez utiliser des listes d’affichage pour réduire le trafic réseau dans les environnements client/serveur. Le contenu d’une liste d’affichage peut être prétraité et peut donc s’exécuter plus efficacement que le même jeu de commandes OpenGL exécuté en mode immédiat. Ce prétraitement est particulièrement important pour le calcul de commandes intensives telles que [**glTexImage**](glteximage1d.md).

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**tramage**
</dt> <dd>

Technique pour l’amélioration de la plage de couleurs perçue dans une image au détriment de la résolution spatiale. Des valeurs de couleur différentes sont affectées aux pixels adjacents. Lorsqu’ils sont affichés à distance, ces couleurs semblent fusionner en une seule couleur intermédiaire. La technique est similaire au demi-virage utilisé dans les publications en noir et blanc pour obtenir des nuances de gris.

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double mise en mémoire tampon**
</dt> <dd>

À l’aide de contextes OpenGL dans lesquels les deux mémoires tampons de couleur d’arrière-plan et d’arrière-plan sont double mise en mémoire tampon. L’animation lisse s’effectue en rendant uniquement la mémoire tampon d’arrière-plan (qui n’est pas affichée), puis en provoquant l’échange des mémoires tampons avant et arrière.

</dd> </dl>

 

 




