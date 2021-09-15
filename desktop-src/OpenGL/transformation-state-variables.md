---
title: Transformation, variables d’état
description: Transformation, variables d’état
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variables d’état de transformation OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b53e0abae08447df86d8968a33a361be08a1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311642"
---
# <a name="transformation-state-variables"></a>Transformation, variables d’état

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_matrice MODELVIEW \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Pile de matrices Modelview             |
| Groupe d’attributs : |                                    |
| Valeur initiale :   | Identité                           |
| Commande d’extraction :     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matrice de projection GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Pile de matrice de projection                                                        |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   | Identité                                                                       |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matrice de texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Pile de matrices de texture                                                           |
| Groupe d’attributs : |                                                                                |
| Valeur initiale :   | Identité                                                                       |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_fenêtre d’affichage comptabilité</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Origine de la fenêtre d’affichage et étendue                                                       |
| Groupe d’attributs : | fenêtre d'affichage                                                                         |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_plage de profondeur GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Plage de profondeur proche et éloignée                                                       |
| Groupe d’attributs : | fenêtre d'affichage                                                                       |
| Valeur initiale :   | 0, 1                                                                           |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>profondeur de la \_ pile MODELVIEW GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Pointeur de pile de matrices Modelview                                                   |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 1                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>profondeur de la \_ pile de projection GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Pointeur de pile de la matrice de projection                                                  |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 1                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>profondeur de la \_ pile de textures GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Pointeur de pile de matrice de texture                                                     |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   | 1                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_mode de matrice du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Mode matrice actuel                                                              |
| Groupe d’attributs : | transformation                                                                        |
| Valeur initiale :   | \_MODELVIEW GL                                                                    |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>normalisation du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|-------------------------------------|
| Description :     | Normalisation normale active/inactive |
| Groupe d’attributs : | transformation/activation                    |
| Valeur initiale :   | GL- \_ faux                           |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plan de clip GL \_ *i*</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------------|
| Description :     | Coefficients de plan de découpage utilisateur         |
| Groupe d’attributs : | transformation                                |
| Valeur initiale :   | 0, 0, 0, 0                               |
| Commande d’extraction :     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plan de clip GL \_ *i*</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | *mon* plan de découpage d’utilisateur est activé |
| Groupe d’attributs : | transformation/activation                   |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




