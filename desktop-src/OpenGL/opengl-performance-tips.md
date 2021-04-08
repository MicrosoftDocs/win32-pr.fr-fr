---
title: Conseils sur les performances OpenGL
description: Conseils sur les performances OpenGL
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, conseils sur les performances
- OpenGL, meilleures pratiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673262"
---
# <a name="opengl-performance-tips"></a>Conseils sur les performances OpenGL

Ces pratiques de programmation optimisent les performances de votre application :

-   Utilisez [**glColorMaterial**](glcolormaterial.md) quand une seule propriété de matériau est modifiée rapidement (par exemple, à chaque vertex). Utilisez [**glMaterial**](glmaterial-functions.md) pour les modifications peu fréquentes ou lorsque plusieurs propriétés de matériau sont modifiées rapidement.
-   Utilisez [**glLoadIdentity**](glloadidentity.md) pour initialiser une matrice, plutôt que de charger votre propre copie de la matrice d’identité.
-   Utilisez des appels de matrice spécifiques tels que [**glRotate**](glrotate.md), [**glTranslate**](gltranslate.md)et [**glScale**](glscale.md), plutôt que de composer vos propres matrices de rotation, de translation et de mise à l’échelle et d’appeler [**glMultMatrix**](glmultmatrix.md).
-   Utilisez [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) pour enregistrer et restaurer les valeurs d’État. Utilisez des fonctions de requête uniquement lorsque votre application requiert les valeurs d’État pour ses propres calculs.
-   Utilisez des listes d’affichage pour encapsuler les changements d’État potentiellement gourmands en mémoire. Par exemple, placez tous les appels [**glTexImage**](glteximage1d.md) requis pour spécifier complètement une texture (et éventuellement les appels [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md)et [**glPixelTransfer**](glpixeltransfer.md) associés) dans une liste d’affichage unique. Appelez cette liste d’affichage pour sélectionner la texture.
-   Utilisez des listes d’affichage pour encapsuler les appels de rendu des objets rigides qui seront dessinés à plusieurs reprises.
-   Pour réduire la bande passante réseau dans les environnements client/serveur, utilisez des évaluateurs, même pour des pavages de surface simples.
-   Si possible, pour éviter la surcharge liée à la normalisation du GL \_ , fournissez des normales à la longueur des unités. Comme [**glScale**](glscale.md) requiert presque toujours l’activation \_ de la normalisation GL, évitez d’utiliser **glScale** lors de l’éclairage.
-   Si vous n’avez pas besoin d’un ombrage lissé, définissez [**glShadeModel**](glshademodel.md) sur GL \_ Flat.
-   Utilisez un seul appel [**glClear**](glclear.md) par Frame, si possible. N’utilisez pas **glClear** pour effacer les petites sous-régions des mémoires tampons. Utilisez-le uniquement pour effacer complètement ou presque complètement la mémoire tampon.
-   Pour dessiner plusieurs triangles indépendants, utilisez un seul appel plutôt que plusieurs appels à [**glBegin**](glbegin.md) ( \_ triangles GL) ou un appel à **glBegin** (polygone du GL \_ ). De même

    Pour dessiner un seul triangle, utilisez des \_ TRIangles GL plutôt qu’un \_ polygone GL.

    Utilisez un seul appel à [**glBegin**](glbegin.md) (GL \_ quads) au lieu d’appeler **glBegin** ( \_ polygone GL) à plusieurs reprises.

    Utilisez un seul appel à [**glBegin**](glbegin.md) ( \_ lignes GL) pour dessiner plusieurs segments de ligne indépendants, plutôt que d’appeler **glBegin** (lignes de GL \_ ) plusieurs fois.

-   En général, utilisez les formes vectorielles des commandes pour passer des données précalculées et utilisez les formes scalaires de commandes pour passer des valeurs calculées près du temps d’appel.
-   Évitez d’effectuer des modifications de mode redondantes, telles que la définition de la couleur sur la même valeur entre chaque vertex d’un polygone à ombrage constant.
-   Lorsque vous dessinez ou copiez des images, désactivez la pixellisation et les opérations par fragments pour optimiser les ressources. OpenGL peut appliquer des textures à des images de pixels.

 

 




