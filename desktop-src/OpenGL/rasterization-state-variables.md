---
title: Rastérisation, variables d’état
description: Rastérisation, variables d’état
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Variables d’état de pixellisation OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1586861eee26f93bca85b8c0f03e9f746e983046bbda755b67a792d65d660b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776889"
---
# <a name="rasterization-state-variables"></a>Rastérisation, variables d’état

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>\_taille du point GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Taille du point                         |
| Groupe d’attributs : | point                              |
| Valeur initiale :   | 1.0                                |
| Commande d’extraction :     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_lisser le point GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Alias de point sur                  |
| Groupe d’attributs : | point/activation                       |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_largeur de ligne du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Largeur de ligne                                                                     |
| Groupe d’attributs : | line                                                                           |
| Valeur initiale :   | 1.0                                                                            |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>\_lisser la ligne GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Anticrénelage de ligne activé               |
| Groupe d’attributs : | ligne/activer                        |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_modèle de \_ STIPPLE de ligne GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Stipple de ligne                                                                     |
| Groupe d’attributs : | line                                                                             |
| Valeur initiale :   | du 1                                                                              |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>STIPPLE de la ligne GL- \_ \_ \_ répéter</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Répéter la ligne stipple                                                              |
| Groupe d’attributs : | line                                                                             |
| Valeur initiale :   | 1                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>\_STIPPLE de ligne GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Stipple de ligne activer                |
| Groupe d’attributs : | ligne/activer                        |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>\_visage de CULLING GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Élimination de polygone activée            |
| Groupe d’attributs : | Polygone/activation                     |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_mode de \_ visage d’élimination du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Élimination des polygones frontaux/back-face                                           |
| Groupe d’attributs : | polygon                                                                          |
| Valeur initiale :   | Back. du GL \_                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>\_face avant \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Indicateur de PV/CCW recto face avant                                              |
| Groupe d’attributs : | polygon                                                                          |
| Valeur initiale :   | \_CCW GL                                                                          |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>\_polygones GL \_ lisse</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Anticrénelage de polygone sur            |
| Groupe d’attributs : | Polygone/activation                     |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_mode polygone \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Mode de pixellisation par polygone (avant et arrière)                                      |
| Groupe d’attributs : | polygon                                                                          |
| Valeur initiale :   | remplissage du GL \_                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>\_STIPPLE de polygones GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Activation de Polygon stipple             |
| Groupe d’attributs : | Polygone/activation                     |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 



| Propriété | Valeur |
|------------------|----------------------------------------------------|
| Description :     | Stipple, modèle de polygone                            |
| Groupe d’attributs : | Polygon-stipple                                    |
| Valeur initiale :   | du 1                                                |
| Commande d’extraction :     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




