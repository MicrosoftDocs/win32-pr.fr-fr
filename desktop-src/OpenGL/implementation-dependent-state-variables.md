---
title: Variables d’état dépendantes de l’implémentation
description: Variables d’état dépendantes de l’implémentation
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Variables d’État Implementation-Dependent OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da38f841408bd6ddf481473837f36544d21d896f2764317957c65158be27fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061457"
---
# <a name="implementation-dependent-state-variables"></a>Variables d’état dépendantes de l’implémentation

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>\_lumières max. GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------|
| Description :     | Nombre maximal d’éclairages               |
| Groupe d’attributs : |                                        |
| Valeur initiale :   | 8                                      |
| Commande d’extraction :     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>\_plans de \_ clips \_ Max GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre maximal de plans de découpage de l’utilisateur                                           |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 6                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>\_profondeur de \_ la \_ pile \_ MODELVIEW GL Max</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Profondeur maximale de la pile modelview-Matrix                                             |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 32                                                                               |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>profondeur de la \_ \_ pile de projection Max \_ GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Profondeur maximale de la pile de projection                                            |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 2                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>profondeur de la \_ \_ pile de texture Max \_ . GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Profondeur maximale de la pile de matrices de texture                                            |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 2                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>BITS de sous- \_ Pixel GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits de précision de sous-pixel dans *x* et *y*                              |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 4                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>\_taille maximale de la \_ texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Hauteur ou largeur maximale d’une image de texture (sans bordure)                     |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 64                                                                               |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>\_table de \_ mappage de pixels Max \_ . GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Taille maximale d’une table de traduction **glPixelMap**                               |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 32                                                                               |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>profondeur de la \_ \_ pile de noms Max \_ . GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Profondeur maximale de la pile des noms de sélection                                               |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 64                                                                               |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_imbrication du nombre maximal de \_ listes GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Imbrication maximale des appels de liste d’affichage                                                |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 64                                                                               |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>\_ordre d' \_ évaluation \_ Max GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Ordre polynomial maximal de l’évaluateur                                               |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 8                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>\_fenêtre d’affichage Max GL- \_ \_ estompe</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Dimensions maximales de la fenêtre d’affichage                                                      |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>profondeur de la \_ \_ pile d’attrib Max \_ . GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Profondeur maximale de la pile d’attributs                                             |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 16                                                                               |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>\_ \_ mémoires TAMPONs GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de mémoires tampons auxiliaires                                                      |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 0                                                                                |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>\_mode GL RVBA \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | True si les mémoires tampons de couleur stockent RVBA                                                 |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>\_mode d’index GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | True si les mémoires tampons de couleur stockent les index                                              |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>\_DOUBLEBUFFER GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | True si des mémoires tampons d’arrière-plan et d’arrière-plan existent                                             |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>\_stéréo GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | True si les mémoires tampons de gauche et de droite existent                                           |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   |                                                                                |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>\_plage de \_ tailles de points GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Plage (faible à élevée) de tailles de points avec anticrénelage                                 |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   | 1, 1                                                                           |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>\_granularité de la taille du point GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Granularité de la taille du point anticrénelage                                             |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   |                                                                                |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>\_plage de \_ largeur de ligne GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Plage (faible à élevée) des largeurs de ligne avec anticrénelage                                 |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   | 1, 1                                                                           |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>\_granularité de la largeur de ligne GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Granularité de la largeur de ligne avec anticrénelage                                             |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   |                                                                                |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




