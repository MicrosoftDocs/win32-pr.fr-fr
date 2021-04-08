---
title: Variables d’état d’éclairage
description: Variables d’état d’éclairage
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variables d’état d’éclairage OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841282"
---
# <a name="lighting-state-variables"></a>Variables d’état d’éclairage

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>\_éclairage GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | True si l’éclairage est activé        |
| Groupe d’attributs : | éclairage/activation                    |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_matériau de couleur GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | True si le suivi des couleurs est activé  |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_paramètre de \_ matériau de couleur GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Couleur actuelle de suivi des propriétés de matériau                                       |
| Groupe d’attributs : | éclairage                                                                         |
| Valeur initiale :   | \_ambiants \_ et \_ DIFFUSes du GL                                                        |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_ \_ visage matériel de couleur GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Visages affectés par le suivi des couleurs                                                 |
| Groupe d’attributs : | éclairage                                                                         |
| Valeur initiale :   | \_recto \_ et \_ Back GL                                                             |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiant du GL \_</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Description :     | Couleur du matériau ambiant                   |
| Groupe d’attributs : | éclairage                                 |
| Valeur initiale :   | (0,2, 0,2, 0,2, 1,0)                        |
| Commande d’extraction :     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_diffusion GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Description :     | Couleur du matériau diffus                   |
| Groupe d’attributs : | éclairage                                 |
| Valeur initiale :   | (0,8, 0,8, 0,8, 1,0)                        |
| Commande d’extraction :     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_spéculaire GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Description :     | Couleur de matériau spéculaire                  |
| Groupe d’attributs : | éclairage                                 |
| Valeur initiale :   | (0.0, 0.0, 0.0, 1.0)                        |
| Commande d’extraction :     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>\_émission GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Description :     | Couleur de matériau émissif                  |
| Groupe d’attributs : | éclairage                                 |
| Valeur initiale :   | (0.0, 0.0, 0.0, 1.0)                        |
| Commande d’extraction :     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>\_éclat GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Description :     | Exposant spéculaire du matériau            |
| Groupe d’attributs : | éclairage                                 |
| Valeur initiale :   | 0.0                                      |
| Commande d’extraction :     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>ambiant (GL \_ Light \_ Model) \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Couleur de scène ambiante                                                            |
| Groupe d’attributs : | éclairage                                                                       |
| Valeur initiale :   | (0,2, 0,2, 0,2, 1,0)                                                              |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ visionneuse locale du modèle de lumière \_ GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Description :     | La visionneuse est locale                                                                  |
| Groupe d’attributs : | éclairage                                                                         |
| Valeur initiale :   | GL- \_ faux                                                                        |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>\_ \_ côté 2 du modèle GL clair \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Utiliser l’éclairage à deux côtés                                                           |
| Groupe d’attributs : | éclairage                                                                         |
| Valeur initiale :   | GL- \_ faux                                                                        |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiant du GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Intensité ambiante de la lumière *i*     |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | (0.0, 0.0, 0.0, 1.0)                  |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>\_diffusion GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Intensité diffuse de la lumière *i*     |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   |                                    |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_spéculaire GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Intensité spéculaire de la lumière *i*    |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   |                                    |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>\_position GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Position de la lumière *i*              |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | (0.0, 0.0, 1.0, 0.0)                  |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atténuation constante du GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Facteur d’atténuation constant        |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | 1.0                                |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atténuation linéaire du GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Facteur d’atténuation linéaire          |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | 0.0                                |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atténuation quadratique du \_ GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Facteur d’atténuation quadratique       |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | 0.0                                |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>\_sens du spot GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Direction Spotlight de la lumière *i*   |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | (0.0, 0.0,-1,0)                     |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>exposant de point comptable \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Exposant Gong de la lumière *i*    |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | 0.0                                |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>coupure de l' \_ emplacement GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | Angle Spotlight de la lumière *i*       |
| Groupe d’attributs : | éclairage                           |
| Valeur initiale :   | 180,0                              |
| Commande d’extraction :     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ clair *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Description :     | True si l’option Light *i* est activée          |
| Groupe d’attributs : | éclairage/activation                    |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_index de couleurs GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Description :     | *C (a)*, *c (d)* et *c (s)* pour l’éclairage d’index de couleurs                         |
| Groupe d’attributs : | éclairage/activation                                                                |
| Valeur initiale :   | 0, 1, 1                                                                          |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




