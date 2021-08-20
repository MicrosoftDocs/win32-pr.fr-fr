---
title: Densité de pixels, variables d’état dépendantes de l’implémentation
description: Densité de pixels, variables d’état dépendantes de l’implémentation
ms.assetid: 3e1de9fe-dce5-437f-ae21-875958660da9
keywords:
- Implementation-Dependent les variables d’État Pixel-Depth OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent Pixel-Depth State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 556e95ae587f44bf41fc1d6f3e9dd0e2fc1351c8dcef9171ffb5d6dba7de134d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554089"
---
# <a name="implementation-dependent-pixel-depth-state-variables"></a>Densité de pixels, variables d’état dépendantes de l’implémentation

<dl> <dt><span id="GL_RED_BITS"></span><span id="gl_red_bits"></span>\_bits rouges \_</dt> <dd> 

| Propriété | Valeur |
|------------------|---------------------------------------------------|
| Description :     | Nombre de bits par composant rouge dans les mémoires tampons de couleur |
| Groupe d’attributs : |                                                   |
| Valeur initiale :   |                                                   |
| Commande d’extraction :     | [**glGetIntegerv**](glgetintegerv.md)            |



 

</dd> <dt><span id="GL_GREEN_BITS"></span><span id="gl_green_bits"></span>\_bits verts du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant vert dans les mémoires tampons de couleur                              |
| Groupe d’attributs : |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |
| Valeur initiale :   |                                                                                  |



 

</dd> <dt><span id="GL_BLUE_BITS"></span><span id="gl_blue_bits"></span>\_bits bleus du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant bleu dans les mémoires tampons de couleur                               |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_BITS"></span><span id="gl_alpha_bits"></span>\_bits alpha \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant alpha dans les mémoires tampons de couleur                              |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_BITS"></span><span id="gl_index_bits"></span>\_bits d’index GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par index dans les mémoires tampons de couleurs                                        |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_BITS"></span><span id="gl_depth_bits"></span>\_bits de profondeur GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bitplanes de mémoire tampon de profondeur                                                 |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_BITS"></span><span id="gl_stencil_bits"></span>\_bits de stencil du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bitplanes de stencil                                                      |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_RED_BITS"></span><span id="gl_accum_red_bits"></span>\_ \_ bits en rouge cumulé \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant rouge dans la mémoire tampon d’accumulation                      |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_GREEN_BITS"></span><span id="gl_accum_green_bits"></span>\_bits cumulés \_ verts \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant vert dans la mémoire tampon d’accumulation                    |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_BLUE_BITS"></span><span id="gl_accum_blue_bits"></span>\_ \_ bits de poids total du GL cumulé \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant bleu dans la mémoire tampon d’accumulation                     |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_ALPHA_BITS"></span><span id="gl_accum_alpha_bits"></span>\_bits amort \_ alpha \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Nombre de bits par composant alpha dans la mémoire tampon d’accumulation                    |
| Groupe d’attributs : |                                                                                  |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




