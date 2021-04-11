---
title: C (OpenGL)
description: Définitions des termes OpenGL qui commencent par la lettre C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- ordinateurs clients
- mémoire du client
- coordonnées du clip
- découper
- index des couleurs
- mode d’index des couleurs
- cartes de couleur
- components
- contextes
- frontière
- enveloppe convexe
- système de coordonnées
- élimination
- matrice actuelle
- position du raster actuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032252"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [e](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**ordinateur client**
</dt> <dd>

Ordinateur à partir duquel les commandes OpenGL sont émises. L’ordinateur qui émet des commandes OpenGL peut être connecté via un réseau à un autre ordinateur qui exécute les commandes, ou les commandes peuvent être émises et exécutées sur le même ordinateur. Voir aussi [serveur](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**mémoire du client**
</dt> <dd>

La mémoire principale (où les variables de programme sont stockées) de l’ordinateur client.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordonnées du clip**
</dt> <dd>

Système de coordonnées qui suit la transformation par la matrice de projection et précède la Division de perspective. Vue-le découpage du volume est effectué en coordonnées de clip, mais pas le découpage propre à l’application. Voir aussi [découpage propre à l’application](a.md).

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**portion**
</dt> <dd>

Suppression de la partie d’une primitive géométrique qui est en dehors du demi-espace défini par un plan de découpage. Les points sont simplement rejetés en dehors de. La partie d’une ligne ou d’un polygone qui est en dehors du demi-espace est éliminée, et des vertex supplémentaires sont générés si nécessaire pour terminer la primitive dans le demi-espace de découpage. Les primitives géométriques et la position raster actuelle (lorsqu’elles sont spécifiées) sont toujours coupées par rapport aux six demi-espaces définis par les plans gauche, droit, inférieur, supérieur, proche et Far du volume de la vue. Les applications peuvent spécifier des plans de découpage spécifiques à l’application facultatifs à appliquer dans les coordonnées oculaires.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**index des couleurs**
</dt> <dd>

Valeur unique qui représente une couleur par nom, plutôt que par valeur. Les index de couleurs OpenGL sont traités comme des valeurs continues (par exemple, des nombres à virgule flottante), tandis que des opérations telles que l’interpolation et le tramage sont effectuées sur ces derniers. Toutefois, les index de couleurs stockés dans la mémoire tampon de trame sont toujours des valeurs entières. Les index à virgule flottante sont convertis en entiers en arrondissant à la valeur entière la plus proche.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**mode d’index des couleurs**
</dt> <dd>

Mode d’un contexte OpenGL dans lequel ses mémoires tampons de couleur stockent les index de couleur, plutôt que les composants de couleur rouge, vert, bleu et alpha.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**carte des couleurs**
</dt> <dd>

Tableau de mappages index-à-RGB accessibles par le matériel d’affichage. Chaque index de couleur est lu à partir de la mémoire tampon de couleur, converti en une triple RVB par recherche dans la carte des couleurs, puis envoyé à l’analyse.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**-**
</dt> <dd>

Valeur unique, continue (par exemple, à virgule flottante) qui représente une intensité ou une quantité. En règle générale, une valeur de composant égale à zéro représente la valeur ou l’intensité minimale, et une valeur de composant égale à 1 représente la valeur ou l’intensité maximale, même si d’autres normalisations sont parfois utilisées. Étant donné que les valeurs des composants sont interprétées dans une plage normalisée, elles sont spécifiées indépendamment de la résolution réelle. Par exemple, le triple RVB (1, 1, 1) est blanc, que les tampons de couleur stockent 4, 8 ou 12 bits chacun. Les composants hors limites sont généralement ancrés à la plage normalisée, non tronqués ou interprétés autrement. Par exemple, la triple RGB (1,4, 1,5, 0,9) est ancrée (1,0, 1,0, 0,9) avant d’être utilisée pour mettre à jour la mémoire tampon de couleur. Les niveaux rouge, vert, bleu, alpha et profondeur sont toujours traités en tant que composants, jamais en tant qu’index.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**contexte**
</dt> <dd>

Ensemble complet de variables d’État OpenGL. Notez que le contenu de trame ne fait pas partie de l’État OpenGL, mais que la configuration du trame est.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**frontière**
</dt> <dd>

Condition d’un polygone dans laquelle aucune ligne droite dans le plan du polygone ne croise le polygone plus de deux fois.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**forme convexe**
</dt> <dd>

Plus petite région convexe englobant un groupe de points spécifié. Dans deux dimensions, la forme convexe est trouvée d’un point de vue conceptuel en étirant une bande caoutchoutée autour des points afin que tous les points se trouvent dans la bande.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**système de coordonnées**
</dt> <dd>

Dans un espace en n dimensions, ensemble de n vecteurs linéairement indépendants ancrés à un point (appelé « origine »). Un groupe de coordonnées spécifie un point dans l’espace n-dimensionnel, un ensemble de n vecteurs linéairement indépendants ancrés à un point (appelé « origine »). Un groupe de coordonnées spécifie un point dans l'espace (ou un vecteur partant de l'origine) en indiquant la distance à parcourir le long de chaque vectoriel pour atteindre le point (ou pointe du vecteur). (ou un vecteur à partir de l’origine) en indiquant la distance de déplacement le long de chaque vecteur pour atteindre le point (ou l’extrémité du vecteur).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**élimination**
</dt> <dd>

Processus d’élimination d’une facette ou d’un arrière-plan d’un polygone afin que la face ne soit pas dessinée.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matrice actuelle**
</dt> <dd>

Matrice qui transforme les coordonnées d’un système de coordonnées en coordonnées d’un autre système. OpenGL contient trois matrices actuelles : la matrice modelview, qui transforme les coordonnées des objets (coordonnées spécifiées par le programmeur) en coordonnées oculaires ; la matrice de perspective, qui transforme les coordonnées oculaire en coordonnées de clip ; et la matrice de texture, qui transforme les coordonnées de texture spécifiées ou générées comme décrit par la matrice. Chaque matrice actuelle est le premier élément d’une pile de matrices. Chacune des trois piles peut être manipulée avec les commandes de manipulation de matrice OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**position du raster actuel**
</dt> <dd>

Position de la coordonnée de la fenêtre qui spécifie le positionnement d’une primitive d’image lorsqu’elle est pixellisée. La position actuelle du raster, ainsi que les autres paramètres de trame actuels, sont mis à jour lorsque glRasterpos est appelé.

</dd> </dl>

 

 




