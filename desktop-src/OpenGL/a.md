---
title: A (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- alias
- alpha
- animation
- anticrénelage
- découpage spécifique à l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb69307f869031bb9fd176ec85dd20eac5d543ef3e7f63086c6ea0801d1b8b8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128369"
---
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**alias**
</dt> <dd>

Technique de rendu qui attribue aux pixels la couleur de la primitive rendue, que cette primitive couvre tout ou partie de la zone du pixel. L’alias génère des bords dentelés ou des escalier. Voir aussi en [escalier](jk.md).

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**lettres**
</dt> <dd>

Quatrième composant de couleur généralement utilisé pour contrôler la fusion des couleurs. Le composant alpha n’est jamais affiché directement. Par Convention, OpenGL alpha indique l’opacité et la transparence sur une échelle de 0,0 à 1,0. Une valeur alpha de 1,0 implique une opacité complète, une valeur alpha de 0,0 implique une transparence complète.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**Animation**
</dt> <dd>

Génération d’un rendu répété d’une scène suffisamment rapidement, avec des positions de point de vue et d’objet en constante évolution, que l’illusion de mouvement est obtenue. L’animation OpenGL utilise presque toujours la double mise en mémoire tampon.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**anticrénelage**
</dt> <dd>

Technique de rendu qui assigne des couleurs aux pixels en fonction de la fraction de la zone de pixels couverte par la primitive rendue. Le rendu avec anticrénelage réduit ou élimine les escalier qui résultent d’un rendu avec alias. Voir aussi [irrégularités](jk.md), [rendu](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**découpage spécifique à l’application** 
</dt> <dd>

Découpage des primitives par rapport aux plans en coordonnées oculaires. Les plans sont spécifiés par l’application à l’aide de [**glClipPlane**](glclipplane.md). Voir aussi [coordonnées oculaires](e.md).

</dd> </dl>

 

 




