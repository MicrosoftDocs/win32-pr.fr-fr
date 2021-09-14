---
title: Texture, variables d’état
description: Texture, variables d’état
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variables d’état de texturage OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff468c701100cc598a519ed3aa290913016a559e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311653"
---
# <a name="texturing-state-variables"></a>Texture, variables d’état

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Texture GL \_ *x*</dt> <dd> 

| Propriété | Valeur |
|------------------|-------------------------------------------------------|
| Description :     | True si la texture *x* -d est activée (*x* est 1-D ou 2D-d) |
| Groupe d’attributs : | texture/activation                                        |
| Valeur initiale :   | GL- \_ faux                                             |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_texture GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------|
| Description :     | image de texture *x* -D au niveau de détail *i* |
| Groupe d’attributs : |                                              |
| Valeur initiale :   |                                              |
| Commande d’extraction :     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>largeur de la \_ texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------|
| Description :     | largeur *de l’image* de texture *x* -D                       |
| Groupe d’attributs : |                                                          |
| Valeur initiale :   | 0                                                        |
| Commande d’extraction :     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>hauteur de la \_ texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------|
| Description :     | hauteur *de l’image* de texture *x* -D                      |
| Groupe d’attributs : |                                                          |
| Valeur initiale :   | 0                                                        |
| Commande d’extraction :     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>bordure de la \_ texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------|
| Description :     | bordure *de l’image* de texture *x* -D                      |
| Groupe d’attributs : |                                                          |
| Valeur initiale :   | 0                                                        |
| Commande d’extraction :     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_composants de texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------|
| Description :     | Composants d’image de texture                                 |
| Groupe d’attributs : |                                                          |
| Valeur initiale :   | 1                                                        |
| Commande d’extraction :     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>couleur de bordure de la \_ texture GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------------------|
| Description :     | Couleur de bordure de la texture                           |
| Groupe d’attributs : | texture                                        |
| Valeur initiale :   | 0, 0, 0, 0                                     |
| Commande d’extraction :     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>filtre de la \_ texture GL \_ min. \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------------------|
| Description :     | Fonction de réduction de texture                  |
| Groupe d’attributs : | texture                                        |
| Valeur initiale :   | MIPMAP linéaire de la comptabilité la \_ plus proche \_ \_                    |
| Commande d’extraction :     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>filtre de la \_ texture GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------------------|
| Description :     | Fonction d’agrandissement de texture                 |
| Groupe d’attributs : | texture                                        |
| Valeur initiale :   | linéaire du GL \_                                     |
| Commande d’extraction :     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>\_Enveloppe de \_ la texture GL \_ *x*</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------------------|
| Description :     | Mode habillage de la texture (*x* est S ou T)              |
| Groupe d’attributs : | texture                                        |
| Valeur initiale :   | répétition du GL \_                                     |
| Commande d’extraction :     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_ \_ mode env de la texture GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------|
| Description :     | Fonction d’application de texture         |
| Groupe d’attributs : | texture                              |
| Valeur initiale :   | module comptabilité GL \_                         |
| Commande d’extraction :     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>couleur de la texture du GL \_ \_ env \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------|
| Description :     | Couleur de l’environnement de texture            |
| Groupe d’attributs : | texture                              |
| Valeur initiale :   | 0, 0, 0, 0                           |
| Commande d’extraction :     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ texture \_ GEN \_ *x*</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------------|
| Description :     | Texgen est activé (*x* est S, T, R ou Q) |
| Groupe d’attributs : | texture/activation                           |
| Valeur initiale :   | GL- \_ faux                                |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plan oculaire \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------|
| Description :     | Coefficients d’équation du plan Texgen   |
| Groupe d’attributs : | texture                              |
| Valeur initiale :   |                                      |
| Commande d’extraction :     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plan d’objet GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------|
| Description :     | Objets Texgen-coefficients linéaires    |
| Groupe d’attributs : | texture                              |
| Valeur initiale :   |                                      |
| Commande d’extraction :     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_mode de génération de textures GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------|
| Description :     | Fonction utilisée pour texgen             |
| Groupe d’attributs : | texture                              |
| Valeur initiale :   | linéaire de l' \_ oeil GL \_                      |
| Commande d’extraction :     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




