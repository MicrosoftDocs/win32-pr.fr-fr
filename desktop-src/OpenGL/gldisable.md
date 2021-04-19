---
title: fonction glDisable (GL. h)
description: Les fonctions glEnable et glDisable activent ou désactivent les fonctionnalités OpenGL. | fonction glDisable (GL. h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- glDisable fonction OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522324"
---
# <a name="gldisable-function"></a>glDisable fonction)

Les fonctions [**glEnable**](glenable.md) et **glDisable** activent ou désactivent les fonctionnalités OpenGL.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*encapsul* 
</dt> <dd>

Constante symbolique indiquant une fonctionnalité OpenGL.

Pour plus d’informations sur *les valeurs que* peut prendre, consultez la section Notes suivante.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | *Cap* ne faisait pas partie des valeurs listées dans la section Notes précédente.<br/>                                                   |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

Les fonctions [**glEnable**](glenable.md) et **glDisable** activent et désactivent différentes fonctionnalités graphiques OpenGL. Utilisez [**glIsEnabled**](glisenabled.md) ou [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) pour déterminer la valeur actuelle de toutes les fonctionnalités.

[**GlEnable**](glenable.md) et **glDisable** prennent tous deux un seul argument, *Cap*, qui peut prendre l’une des valeurs suivantes :



| Valeur                       | Signification                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TEST du GL \_ alpha \_             | S’il est activé, effectuez des tests alpha. Consultez [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| \_standard GL Auto \_            | Si cette option est activée, les vecteurs normaux de la surface de calcul sont analytiquement quand le map2 de l’analyse de la valeur de vertex \_ \_ \_ 3 ou GL \_ map2 \_ vertex \_ 4 a généré des vertex. Consultez [**glMap2**](glmap2.md).                                                                                        |
| fusion du GL \_                   | S’il est activé, fusionne les valeurs de couleur RVBA entrantes avec les valeurs des mémoires tampons de couleur. Consultez [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| \_Plan de clip GL \_ *i*          | S’il est activé, découpez la géométrie par rapport au plan de découpage défini par l’utilisateur *i*. Consultez [**glClipPlane**](glclipplane.md).                                                                                                                                                  |
| GL \_ Color \_ Logic \_ op        | S’il est activé, applique l’opération logique actuelle aux valeurs de la couleur RVBA entrante et de la mémoire tampon de couleur. Consultez [**glLogicOp**](gllogicop.md).                                                                                                                     |
| \_matériau de couleur GL \_         | S’il est activé, un ou plusieurs paramètres de matériau suivent la couleur actuelle. Consultez [**glColorMaterial**](glcolormaterial.md).                                                                                                                                   |
| \_visage de CULLING GL \_              | S’il est activé, les polygones sont supprimés en fonction de leur enroulement dans les coordonnées de la fenêtre. Consultez [**glCullFace**](glcullface.md).                                                                                                                                               |
| \_test de profondeur du GL \_             | S’il est activé, effectuez des comparaisons de profondeur et mettez à jour le tampon de profondeur. Consultez [**glDepthFunc**](gldepthfunc.md) et [**glDepthRange**](gldepthrange.md).                                                                                                              |
| \_tramage GL                  | S’il est activé, les composants ou les index de couleur de tramage avant leur écriture dans la mémoire tampon de couleur.                                                                                                                                                                 |
| \_brouillard GL                     | S’il est activé, fusionne une couleur de brouillard dans la couleur de l’après-texturation. Consultez [**glFog**](glfog.md).                                                                                                                                                                    |
| logique d’index GL- \_ \_ \_ op        | S’il est activé, applique l’opération logique actuelle à l’index entrant et aux index de la mémoire tampon des couleurs. Consultez [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ clair *i*                | S’il est activé, incluez le *i* clair dans l’évaluation de l’équation d’éclairage. Consultez [**glLightModel**](gllightmodel-functions.md) et [**glLight**](gllight-functions.md).                                                                                      |
| \_éclairage GL                | S’il est activé, utilisez les paramètres d’éclairage actuels pour calculer la couleur ou l’index du vertex. S’il est désactivé, associe la couleur ou l’index actuel à chaque vertex. Consultez [**glMaterial**](glmaterial-functions.md), **glLightModel** et **glLight**.                |
| \_lisser la ligne GL \_            | S’il est activé, dessinez des lignes avec un filtrage correct. S’il est désactivé, dessinez des lignes avec des alias. Consultez [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| \_STIPPLE de ligne GL \_           | S’il est activé, utilisez le modèle de stipple de la ligne active lors du dessin de lignes. Consultez [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| GL \_ logique \_ op               | S’il est activé, applique l’opération logique actuellement sélectionnée aux index de mémoire tampon entrante et de couleur. Consultez [**glLogicOp**](gllogicop.md).                                                                                                                    |
| Map1 GL- \_ \_ couleur \_ 4          | S’il est activé, les appels à [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)et [**GLEVALPOINT1**](glevalpoint.md) génèrent des valeurs RVBA. Voir aussi [**glMap1**](glmap1.md).                                           |
| \_Index Map1 \_ GL             | S’il est activé, les appels à **glEvalCoord1**, **glEvalMesh1** et **glEvalPoint1** génèrent des index de couleurs. Voir aussi **glMap1**.                                                                                                                                   |
| Map1 GL- \_ \_ normal            | S’il est activé, les appels à [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)et [**glEvalPoint1**](glevalpoint.md) génèrent des normales. Voir aussi [**glMap1**](glmap1.md).                                               |
| \_Repère de \_ texture Map1 GL \_ \_ 1 | S’il est activé, les appels à **glEvalCoord1**, **glEvalMesh1** et **glEvalPoint1** génèrent des coordonnées de texture *s* . Voir aussi **glMap1**.                                                                                                                         |
| \_Map1 de \_ texture \_ GL \_ 2 | S’il est activé, les appels à [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)et [**glEvalPoint1**](glevalpoint.md) génèrent des coordonnées de texture *s* et *t* . Voir aussi [**glMap1**](glmap1.md).                       |
| \_Repère de \_ texture Map1 GL \_ \_ 3 | S’il est activé, les appels à **glEvalCoord1**, **glEvalMesh1** et **glEvalPoint1** génèrent des coordonnées de texture *s*, *t* et *r* . Voir aussi **glMap1**.                                                                                                           |
| \_Map1 de \_ texture \_ GL \_ 4 | S’il est activé, les appels à [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)et [**glEvalPoint1**](glevalpoint.md) génèrent des coordonnées de texture *s*, *t*, *r* et *q* . Voir aussi [**glMap1**](glmap1.md).                    |
| Map1 du GL- \_ \_ vertex \_ 3         | Si cette option est activée, les appels à **glEvalCoord1**, **glEvalMesh1** et **glEvalPoint1** génèrent des coordonnées de vertex *x*, *y* et *z* . Voir aussi **glMap1**.                                                                                                            |
| Map1 du GL- \_ \_ vertex \_ 4         | Si cette option est activée, les appels à [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)et [**glEvalPoint1**](glevalpoint.md) génèrent des coordonnées de vertex *x*, *y*, *z* et *w* homogènes. Voir aussi [**glMap1**](glmap1.md). |
| Map2 GL- \_ \_ couleur \_ 4          | S’il est activé, les appels à [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)et [**GLEVALPOINT2**](glevalpoint.md) génèrent des valeurs RVBA. Voir aussi [**glMap2**](glmap2.md).                                           |
| \_Index map2 \_ GL             | S’il est activé, les appels à **glEvalCoord2**, **glEvalMesh2** et **glEvalPoint2** génèrent des index de couleurs. Voir aussi **glMap2**.                                                                                                                                   |
| Map2 GL- \_ \_ normal            | S’il est activé, les appels à [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)et [**glEvalPoint2**](glevalpoint.md) génèrent des normales. Voir aussi [**glMap2**](glmap2.md).                                               |
| \_Repère de \_ texture map2 GL \_ \_ 1 | S’il est activé, les appels à **glEvalCoord2**, **glEvalMesh2** et **glEvalPoint2** génèrent des coordonnées de texture *s* . Voir aussi **glMap2**.                                                                                                                         |
| \_Map2 de \_ texture \_ GL \_ 2 | S’il est activé, les appels à [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)et [**glEvalPoint2**](glevalpoint.md) génèrent des coordonnées de texture *s* et *t* . Voir aussi [**glMap2**](glmap2.md).                       |
| \_Repère de \_ texture map2 GL \_ \_ 3 | S’il est activé, les appels à **glEvalCoord2**, **glEvalMesh2** et **glEvalPoint2** génèrent des coordonnées de texture *s*, *t* et *r* . Voir aussi **glMap2**.                                                                                                           |
| \_Map2 de \_ texture \_ GL \_ 4 | S’il est activé, les appels à [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)et [**glEvalPoint2**](glevalpoint.md) génèrent des coordonnées de texture *s*, *t*, *r* et *q* . Voir aussi [**glMap2**](glmap2.md).            |
| Map2 du GL- \_ \_ vertex \_ 3         | Si cette option est activée, les appels à **glEvalCoord2**, **glEvalMesh2** et **glEvalPoint2** génèrent des coordonnées de vertex *x*, *y* et *z* . Voir aussi **glMap2**.                                                                                                            |
| Map2 du GL- \_ \_ vertex \_ 4         | Si cette option est activée, les appels à [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)et [**glEvalPoint2**](glevalpoint.md) génèrent des coordonnées de vertex *x*, *y*, *z* et *w* homogènes. Voir aussi [**glMap2**](glmap2.md). |
| normalisation du GL \_               | Si cette option est activée, les vecteurs normaux spécifiés avec **glNormal** sont mis à l’échelle en fonction de la longueur de l’unité après la transformation. Consultez [**glNormal**](glnormal-functions.md).                                                                                                          |
| \_lisser le point GL \_           | S’il est activé, dessinez des points avec un filtrage correct. S’il est désactivé, dessinez des points d’alias. Consultez [**glPointSize**](glpointsize.md).                                                                                                                                    |
| \_remplissage du \_ décalage du polygone GL \_   | S’il est activé, et si le polygone est rendu en \_ mode de remplissage GL, un décalage est ajouté aux valeurs de profondeur des fragments d’un polygone avant l’exécution de la comparaison de profondeur. Consultez [**glPolygonOffset**](glpolygonoffset.md)**.**                                      |
| \_ligne de \_ décalage du polygone GL \_   | S’il est activé, et si le polygone est rendu en \_ mode de ligne GL, un décalage est ajouté aux valeurs de profondeur des fragments d’un polygone avant l’exécution de la comparaison de profondeur. Consultez **glPolygonOffset**.                                                                 |
| \_point de \_ décalage du polygone GL \_  | Si cette option est activée, un décalage est ajouté aux valeurs de profondeur des fragments d’un polygone avant l’exécution de la comparaison de profondeur, si le polygone est rendu en \_ mode point GL. Consultez [**glPolygonOffset**](glpolygonoffset.md).                                             |
| \_polygones GL \_ lisse         | S’il est activé, dessinez les polygones avec le filtrage approprié. S’il est désactivé, dessinez des polygones avec alias. Consultez [**glPolygonMode**](glpolygonmode.md).                                                                                                                            |
| \_STIPPLE de polygones GL \_        | S’il est activé, utilisez le modèle stipple Polygon actuel lors du rendu de polygones. Consultez [**glPolygonStipple**](glpolygonstipple.md).                                                                                                                              |
| \_test de ciseaux du GL \_           | S’il est activé, ignorer les fragments qui sont en dehors du rectangle de la ciseaux. Consultez [**glScissor**](glscissor.md).                                                                                                                                                   |
| \_test du stencil du GL \_           | S’il est activé, effectue le test stencil et met à jour la mémoire tampon du stencil. Consultez [**glStencilFunc**](glstencilfunc.md) et [**glStencilOp**](glstencilop.md).                                                                                                            |
| \_Texture GL \_ 1D             | Si cette option est activée, les textures unidimensionnelles sont effectuées (sauf si la texturation à deux dimensions est également activée). Consultez [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| \_Texture GL \_ 2D             | S’il est activé, la texturation à deux dimensions est effectuée. Consultez [**glTexImage2D**](glteximage2d.md).                                                                                                                                                               |
| GL \_ texture \_ GEN \_ Q         | S’il est activé, la coordonnée de texture *q* est calculée à l’aide de la fonction de génération de texture définie avec [**glTexGen**](gltexgen-functions.md). Dans le cas contraire, la coordonnée de texture *q* actuelle est utilisée.                                                        |
| GL \_ texture \_ GEN \_ R         | S’il est activé, la coordonnée de texture *r* est calculée à l’aide de la fonction de génération de texture définie avec [**glTexGen**](gltexgen-functions.md). Si elle est désactivée, la coordonnée de texture *r* actuelle est utilisée.                                                      |
| GL \_ texture \_ GEN \_ S         | S’il est activé, la coordonnée de texture *s* est calculée à l’aide de la fonction de génération de texture définie avec **glTexGen**. Si elle est désactivée, la coordonnée *de texture active* est utilisée.                                                                                |
| GL \_ texture \_ GEN \_ T         | S’il est activé, la coordonnée de texture *t* est calculée à l’aide de la fonction de génération de texture définie avec [**glTexGen**](gltexgen-functions.md). Si elle est désactivée, la coordonnée de texture *t* actuelle est utilisée.                                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothèque<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





