---
title: Variables d’état de contrôle trame
description: Variables d’état de contrôle trame
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variables d’état de contrôle trame OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998414271956de44710e9ef456722d7499adb862
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910077"
---
# <a name="framebuffer-control-state-variables"></a>Variables d’état de contrôle trame

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_mémoire tampon de dessin GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------|
| Description :     | Mémoires tampons sélectionnées pour le dessin           |
| Groupe d’attributs : | mémoire tampon de couleur                           |
| Valeur initiale :   |                                        |
| Commande d’extraction :     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_WRITEMASK d’index GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Writemask d’index de couleurs                                                            |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | du 1                                                                              |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de couleur GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | L’écriture des couleurs active ; R, G, B ou A                                               |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | GL \_ true                                                                         |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_profondeur GL \_ WRITEMASK</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Mémoire tampon de profondeur activée pour l’écriture                                                 |
| Groupe d’attributs : | mémoire tampon de profondeur                                                                     |
| Valeur initiale :   | GL \_ true                                                                         |
| Commande d’extraction :     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_WRITEMASK du stencil du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Stencil-tampon writemask                                                         |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | du 1                                                                              |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ valeur Clear de couleur GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Valeur effacée de la mémoire tampon de couleur (mode RVBA)                                           |
| Groupe d’attributs : | mémoire tampon de couleur                                                                   |
| Valeur initiale :   | 0, 0, 0, 0                                                                     |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ valeur effacer de l’index GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Valeur effacée de la mémoire tampon de couleur (mode index des couleurs)                                    |
| Groupe d’attributs : | mémoire tampon de couleur                                                                   |
| Valeur initiale :   | 0                                                                              |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ valeur effacer de profondeur du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Valeur effacée de la mémoire tampon de profondeur                                                         |
| Groupe d’attributs : | mémoire tampon de profondeur                                                                     |
| Valeur initiale :   | 1                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ valeur effacer du stencil du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Valeur effacer du tampon stencil                                                       |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | 0                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_valeur effacer GL amort \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | Accumulation-valeur effacée de la mémoire tampon                                                |
| Groupe d’attributs : | mémoire tampon cumulée                                                                   |
| Valeur initiale :   | 0                                                                              |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




