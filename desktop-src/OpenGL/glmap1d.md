---
title: glMap1d, fonction (Gl.h)
description: La fonction glMap1d définit un évaluateur unidimensionnel. | fonction glMap1d (GL. h)
ms.assetid: 65f8b099-597c-4300-a7d1-3dabdd19e6cb
keywords:
- glMap1d fonction OpenGL
topic_type:
- apiref
api_name:
- glMap1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35aee409ab814f9ec2f09add79a700fde4b43998
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238398"
---
# <a name="glmap1d-function"></a>glMap1d fonction)

Les fonctions **glMap1d** et [**glMap1f**](glmap1f.md) définissent un évaluateur unidimensionnel.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glMap1d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    stride,
         GLint    order,
   const GLdouble *points
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cible* 
</dt> <dd>

Type de valeurs générées par l’évaluateur. Constantes symboliques. Le paramètre *target* est une constante symbolique qui indique le type de points de contrôle fourni en *points*, ainsi que la sortie générée lorsque le mappage est évalué. Elle peut prendre l’une des neuf valeurs prédéfinies.



| Valeur                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**Map1 du GL- \_ \_ vertex \_ 3**</dt> </dl>                       | Chaque point de contrôle est trois valeurs à virgule flottante représentant *x, y* et *z*. Les commandes [**glVertex3**](glvertex-functions.md) internes sont générées lorsque le mappage est évalué.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**Map1 du GL- \_ \_ vertex \_ 4**</dt> </dl>                       | Chaque point de contrôle est quatre valeurs à virgule flottante représentant *x, y, z* et *w*. Les commandes [**glVertex4**](glvertex-functions.md) internes sont générées lorsque le mappage est évalué.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**\_Index Map1 \_ GL**</dt> </dl>                                 | Chaque point de contrôle est une valeur à virgule flottante unique représentant un index de couleurs. Les commandes [**glIndex**](glindex-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, l’index actuel n’est pas mis à jour avec la valeur de ces commandes **glIndex** .<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**Map1 GL- \_ \_ couleur \_ 4**</dt> </dl>                          | Chaque point de contrôle est quatre valeurs à virgule flottante représentant le rouge, le vert, le bleu et l’alpha. Les commandes [**glColor4**](glcolor-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, la couleur actuelle n’est pas mise à jour avec la valeur de ces commandes **glColor4** .<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**Map1 GL- \_ \_ normal**</dt> </dl>                              | Chaque point de contrôle est trois valeurs à virgule flottante représentant les composants *x, y* et *z* d’un vecteur normal. Les commandes [**glNormal**](glnormal-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, la normale actuelle n’est pas mise à jour avec la valeur de ces commandes **glNormal** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**\_Repère de \_ texture Map1 GL \_ \_ 1**</dt> </dl> | Chaque point de contrôle est une valeur à virgule flottante unique représentant la coordonnée de texture *s* . Les commandes [**glTexCoord1**](gltexcoord-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, les coordonnées de texture actuelles ne sont pas mises à jour avec la valeur de ces commandes **glTexCoord** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**\_Map1 de \_ texture \_ GL \_ 2**</dt> </dl> | Chaque point de contrôle est deux valeurs à virgule flottante représentant les coordonnées de texture *s* et *t* . Les commandes [**glTexCoord2**](gltexcoord-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, les coordonnées de texture actuelles ne sont pas mises à jour avec la valeur de ces commandes **glTexCoord** .<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**\_Repère de \_ texture Map1 GL \_ \_ 3**</dt> </dl> | Chaque point de contrôle est trois valeurs à virgule flottante représentant les coordonnées de texture *s, t* et *r* . Les commandes [**glTexCoord3**](gltexcoord-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, les coordonnées de texture actuelles ne sont pas mises à jour avec la valeur de ces commandes **glTexCoord** .<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**\_Map1 de \_ texture \_ GL \_ 4**</dt> </dl> | Chaque point de contrôle est quatre valeurs à virgule flottante représentant les coordonnées de texture *s, t, r* et *q* . Les commandes [**glTexCoord4**](gltexcoord-functions.md) internes sont générées lorsque le mappage est évalué. Toutefois, les coordonnées de texture actuelles ne sont pas mises à jour avec la valeur de ces commandes **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Mappage linéaire de *u*, tel qu’il est présenté à [**glEvalCoord1**](glevalcoord-functions.md), à *u*^, la variable qui est évaluée par les équations spécifiées par cette commande.

</dd> <dt>

*U2* 
</dt> <dd>

Mappage linéaire de *u*, tel qu’il est présenté à [**glEvalCoord1**](glevalcoord-functions.md), à *u*^, la variable qui est évaluée par les équations spécifiées par cette commande.

</dd> <dt>

*progrès* 
</dt> <dd>

Nombre de valeurs float ou double entre le début d’un point de contrôle et le début de la suivante dans la structure de données référencée en *points*. Cela permet d’incorporer des points de contrôle dans des structures de données arbitraires. La seule contrainte est que les valeurs d’un point de contrôle particulier doivent occuper des emplacements de mémoire contigus.

</dd> <dt>

*order* 
</dt> <dd>

Nombre de points de contrôle. Doit être positif.

</dd> <dt>

*points* 
</dt> <dd>

Pointeur vers le tableau de points de contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | la *cible* n’est pas une valeur acceptée.<br/>                                                                                        |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *U1* était égal à *U2*.<br/>                                                                                                    |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | *Stride* était inférieur au nombre de valeurs dans un point de contrôle.<br/>                                                            |
| <dl> <dt>**\_valeur non valide du GL \_**</dt> </dl>     | la *commande* était inférieure à un ou un \_ ordre d’évaluation Max GL \_ \_ .<br/>                                                                         |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les évaluateurs offrent un moyen d’utiliser le mappage polynomial polynomial ou Rational polynomial pour produire des vertex, des normales, des coordonnées de texture et des couleurs. Les valeurs produites par un évaluateur sont envoyées à d’autres étapes du traitement OpenGL comme si elles avaient été présentées à l’aide de commandes [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)et [**glColor**](glcolor-functions.md) , à ceci près que les valeurs générées ne mettent pas à jour la couleur, les coordonnées de texture ou la normale actuelles.

Toutes les splines polynomiaux polynomiales ou rationnelles de tous les degrés (jusqu’au degré maximal pris en charge par l’implémentation OpenGL) peuvent être décrites à l’aide d’évaluateurs. Celles-ci incluent presque toutes les splines utilisées dans les graphiques informatiques, y compris les splines B, les courbes de Bézier, les splines Hermite, etc.

Les évaluateurs définissent les courbes en fonction des polynomiaux Bernstein. Définir **p** () comme

![Équation représentant la définition de p ().](images/map01.png)

où **R**_i_ est un point de contrôle et () est *le polynomial* Bernstein de degree *n* (*ordre*  = *n* + 1) :

![Équation représentant le polynomial Bernstein de degree n.](images/map02.png)

Rappelez-vous que

![Équations présentant l’équivalence à 1.](images/map03.png)

La fonction **glMap1** est utilisée pour définir la base et spécifier le type de valeurs produites. Une fois défini, une carte peut être activée et désactivée en appelant [**glEnable**](glenable.md) et **glDisable** par le nom de la carte, l’une des neuf valeurs prédéfinies pour la *cible* décrite ci-dessus. La fonction [glEvalCoord1](glevalcoord-functions.md) évalue les mappages unidimensionnels qui sont activés. Quand **glEvalCoord1** présente une valeur *u*, les fonctions Bernstein sont évaluées à l’aide de *u*^, où

![Équation représentant la définition de votre ^.](images/map04.png)

Les paramètres *Stride*, *Order* et *points* définissent l’adressage de tableau pour accéder aux points de contrôle. Le paramètre *points* est l’emplacement du premier point de contrôle, qui occupe un, deux, trois ou quatre emplacements de mémoire contigus, en fonction du mappage défini. Le paramètre *Order* est le nombre de points de contrôle dans le tableau. Le paramètre *Stride* indique le nombre d’emplacements float ou double à faire avancer le pointeur de mémoire interne pour atteindre le point de contrôle suivant.

Comme c’est le cas pour toutes les commandes OpenGL qui acceptent des pointeurs vers des données, c’est comme si le contenu des *points* était copié par **glMap1** avant d’être retourné. Les modifications apportées au contenu des *points* n’ont aucun effet après l’appel de **glMap1** .

Les fonctions suivantes récupèrent les informations relatives à **glMap1**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) avec l’argument de l' \_ ordre d’évaluation Max GL \_ \_

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) avec argument GL \_ Map1 \_ vertex \_ 3

**glIsEnabled** avec argument GL \_ Map1 \_ vertex \_ 4

**glIsEnabled** avec argument GL \_ Map1 \_ index

**glIsEnabled** avec argument GL \_ Map1 \_ couleur \_ 4

**glIsEnabled** avec argument GL \_ Map1 \_ normal

**glIsEnabled** avec argument GL \_ Map1 \_ texture \_ Coord \_ 1

**glIsEnabled** avec argument GL \_ Map1 \_ texture \_ Coord \_ 2

**glIsEnabled** avec argument GL \_ Map1 \_ texture \_ repère \_ 3

**glIsEnabled** avec argument GL \_ Map1 \_ texture \_ Coord \_ 4

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





