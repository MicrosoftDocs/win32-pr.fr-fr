---
title: Variables d’État pour les valeurs actuelles et les données associées
description: Variables d’État pour les valeurs actuelles et les données associées
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- Variables d’État pour les valeurs actuelles et les données associées OpenGL
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 149139bc11698469ce0667c2ecf77bc7ab239adb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908467"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>Variables d’État pour les valeurs actuelles et les données associées

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>\_couleur actuelle du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| Description :     | Couleur actuelle                                                                                                        |
| Groupe d’attributs : | actuels                                                                                                              |
| Valeur initiale :   | 1, 1, 1, 1                                                                                                           |
| Commande d’extraction :     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>\_index actuel du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description :     | Index des couleurs actuelles                                                                                                                                            |
| Groupe d’attributs : | actuels                                                                                                                                                        |
| Valeur initiale :   | 1                                                                                                                                                              |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>coordonnées de la \_ texture actuelle du GL \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Coordonnées de texture actuelles                                                    |
| Groupe d’attributs : | actuels                                                                        |
| Valeur initiale :   | 0, 0, 0, 1                                                                     |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>GL \_ actuel- \_ normal</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Normal actuel                                                                 |
| Groupe d’attributs : | actuels                                                                        |
| Valeur initiale :   | 0, 0, 1                                                                        |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>\_position du raster actuel du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Position du raster actuel                                                        |
| Groupe d’attributs : | actuels                                                                        |
| Valeur initiale :   | 0, 0, 0, 1                                                                     |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>DISTANCE de la \_ \_ trame actuelle du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Distance de trame actuelle                                                        |
| Groupe d’attributs : | actuels                                                                        |
| Valeur initiale :   | 0                                                                              |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>\_couleur de \_ trame \_ actuelle du GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description :     | Couleur associée à la position raster                                                                                                                          |
| Groupe d’attributs : | actuels                                                                                                                                                        |
| Valeur initiale :   | 1, 1, 1, 1                                                                                                                                                     |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>\_index de \_ trame \_ actuel du GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description :     | Index de couleurs associé à la position raster                                                                                                                    |
| Groupe d’attributs : | actuels                                                                                                                                                        |
| Valeur initiale :   | 1                                                                                                                                                              |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>coordonnées de la \_ \_ texture raster actuelle \_ du \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Coordonnées de texture associées à la position raster                            |
| Groupe d’attributs : | actuels                                                                        |
| Valeur initiale :   | 0, 0, 0, 1                                                                     |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>\_position de \_ trame actuelle de GL \_ \_ valide</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Bit de position de trame valide                                                        |
| Groupe d’attributs : | actuels                                                                          |
| Valeur initiale :   | GL \_ true                                                                         |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>\_indicateur de périphérie du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Indicateur de périphérie                                                                        |
| Groupe d’attributs : | actuels                                                                          |
| Valeur initiale :   | GL \_ true                                                                         |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




