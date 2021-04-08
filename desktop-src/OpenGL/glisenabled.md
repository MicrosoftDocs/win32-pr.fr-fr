---
title: fonction glIsEnabled (GL. h)
description: La fonction gllsEnabled teste si une fonctionnalité est activée.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- glIsEnabled fonction OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdb2ba206e0a026aef118b06d66097ade9ba9ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743125"
---
# <a name="glisenabled-function"></a>glIsEnabled fonction)

La fonction **gllsEnabled** teste si une fonctionnalité est activée.

## <a name="syntax"></a>Syntaxe


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*encapsul* 
</dt> <dd>

Constante symbolique indiquant une fonctionnalité OpenGL. Les fonctionnalités suivantes sont acceptées.



| Valeur                                                                                                                                                                                                    | Signification                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**TEST du GL \_ alpha \_**</dt> </dl>                                           | Voir [ **glAlphaFunc**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**\_standard GL Auto \_**</dt> </dl>                                        | Voir [ **glEvalCoord**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**fusion du GL \_**</dt> </dl>                                                           | Voir [ **glBlendFunc**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>* * \_ Plan de découpage GL \_ * i * * *</dt> </dl> | Voir [ **glClipPlane**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_tableau de couleurs GL \_**</dt> </dl>                                        | Voir [ **glColorPointer**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**GL \_ Color \_ Logic \_ op**</dt> </dl>                              | Voir [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**\_matériau de couleur GL \_**</dt> </dl>                               | Voir [ **glColorMaterial**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**\_visage de CULLING GL \_**</dt> </dl>                                              | Voir [ **glCullFace**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**\_test de profondeur du GL \_**</dt> </dl>                                           | Voir [**glDepthFunc**](gldepthfunc.md) et [**glDepthRange**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**\_tramage GL**</dt> </dl>                                                        | Voir [ **glEnable**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**\_brouillard GL**</dt> </dl>                                                                 | Voir [ **glFog**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_tableau d’index GL \_**</dt> </dl>                                        | Voir [ **glIndexPointer**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**logique d’index GL- \_ \_ \_ op**</dt> </dl>                              | Voir [ **glLogicOp**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>* * GL \_ clair * i * * *</dt> </dl>                      | Voir [**glLightModel**](gllightmodel-functions.md) et [**glLight**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**\_éclairage GL**</dt> </dl>                                                  | Consultez [**glMaterial**](glmaterial-functions.md), [**glLightModel**](gllightmodel-functions.md)et [**glLight**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**\_lisser la ligne GL \_**</dt> </dl>                                        | Voir [ **glLineWidth**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**\_STIPPLE de ligne GL \_**</dt> </dl>                                     | Voir [ **glLineStipple**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**Map1 GL- \_ \_ couleur \_ 4**</dt> </dl>                                    | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**\_Index Map1 \_ GL**</dt> </dl>                                           | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**Map1 GL- \_ \_ normal**</dt> </dl>                                        | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**\_Repère de \_ texture Map1 GL \_ \_ 1**</dt> </dl>           | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**\_Map1 de \_ texture \_ GL \_ 2**</dt> </dl>           | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**\_Repère de \_ texture Map1 GL \_ \_ 3**</dt> </dl>           | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**\_Map1 de \_ texture \_ GL \_ 4**</dt> </dl>           | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**Map1 du GL- \_ \_ vertex \_ 3**</dt> </dl>                                 | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**Map1 du GL- \_ \_ vertex \_ 4**</dt> </dl>                                 | Voir [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**Map2 GL- \_ \_ couleur \_ 4**</dt> </dl>                                    | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**\_Index map2 \_ GL**</dt> </dl>                                           | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**Map2 GL- \_ \_ normal**</dt> </dl>                                        | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**\_Repère de \_ texture map2 GL \_ \_ 1**</dt> </dl>           | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**\_Map2 de \_ texture \_ GL \_ 2**</dt> </dl>           | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**\_Repère de \_ texture map2 GL \_ \_ 3**</dt> </dl>           | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**\_Map2 de \_ texture \_ GL \_ 4**</dt> </dl>           | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**Map2 du GL- \_ \_ vertex \_ 3**</dt> </dl>                                 | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**Map2 du GL- \_ \_ vertex \_ 4**</dt> </dl>                                 | Voir [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_tableau normal du GL \_**</dt> </dl>                                     | Voir [ **glNormalPointer**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**normalisation du GL \_**</dt> </dl>                                               | Voir [ **glNormal**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**\_lisser le point GL \_**</dt> </dl>                                     | Voir [ **glPointSize**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**\_remplissage du \_ décalage du polygone GL \_**</dt> </dl>               | Voir [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**\_ligne de \_ décalage du polygone GL \_**</dt> </dl>               | Voir [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**\_point de \_ décalage du polygone GL \_**</dt> </dl>            | Voir [ **glPolygonOffset**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**\_polygones GL \_ lisse**</dt> </dl>                               | Voir [ **glPolygonMode**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**\_STIPPLE de polygones GL \_**</dt> </dl>                            | Voir [ **glPolygonStipple**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**\_test de ciseaux du GL \_**</dt> </dl>                                     | Voir [ **glScissor**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**\_test du stencil du GL \_**</dt> </dl>                                     | Voir [**glStencilFunc**](glstencilfunc.md) et [**glStencilOp**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**\_Texture GL \_ 1D**</dt> </dl>                                           | Voir [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**\_Texture GL \_ 2D**</dt> </dl>                                           | Voir [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**Tableau de coordonnées de la \_ texture GL \_ \_**</dt> </dl>               | Voir [ **glTexCoordPointer**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**GL \_ texture \_ GEN \_ Q**</dt> </dl>                                 | Voir [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**GL \_ texture \_ GEN \_ R**</dt> </dl>                                 | Voir [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**GL \_ texture \_ GEN \_ S**</dt> </dl>                                 | Voir [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**GL \_ texture \_ GEN \_ T**</dt> </dl>                                 | Voir [ **glTexGen**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_tableau de vertex GL \_**</dt> </dl>                                     | Voir [ **glVertexPointer**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Les codes d’erreur suivants peuvent être récupérés par la fonction [**glGetError**](glgeterror.md) .



| Nom                                                                                                  | Signification                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enum GL non valide \_**</dt> </dl>      | l' *embout* n’était pas une valeur acceptée.<br/>                                                                                           |
| <dl> <dt>**\_opération non valide du GL \_**</dt> </dl> | La fonction a été appelée entre un appel à [**glBegin**](glbegin.md) et l’appel correspondant à [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Notes

La fonction **gllsEnabled** retourne GL \_ true si *Cap* est une fonctionnalité activée et retourne la \_ valeur GL false dans le cas contraire.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





