---
title: Évaluateur, variables d’état
description: Évaluateur, variables d’état
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- Variables d’état de l’évaluateur OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2895f773721f7c900003cbaa0f070c277a0e260
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413683"
---
# <a name="evaluator-state-variables"></a>Évaluateur, variables d’état

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>\_commande GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------|
| Description :     | ordre des cartes 1D                  |
| Groupe d’attributs : |                                |
| Valeur initiale :   | 1                              |
| Commande d’extraction :     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>\_commande GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------|
| Description :     | commandes de mappage 2D                 |
| Groupe d’attributs : |                                |
| Valeur initiale :   | 1, 1                            |
| Commande d’extraction :     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>\_Coeff GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------|
| Description :     | points de contrôle 1D             |
| Groupe d’attributs : |                                |
| Valeur initiale :   |                                |
| Commande d’extraction :     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>\_Coeff GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------|
| Description :     | points de contrôle 2D             |
| Groupe d’attributs : |                                |
| Valeur initiale :   |                                |
| Commande d’extraction :     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>\_domaine GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------|
| Description :     | points de terminaison de domaine 1D           |
| Groupe d’attributs : |                                |
| Valeur initiale :   |                                |
| Commande d’extraction :     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>\_domaine GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------|
| Description :     | points de terminaison de domaine 2D           |
| Groupe d’attributs : |                                |
| Valeur initiale :   |                                |
| Commande d’extraction :     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ Map1 \_ x</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | le mappage 1D permet : *x* est un type de mappage   |
| Groupe d’attributs : | eval/Enable                        |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ map2 \_ x</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | mappage 2D active : *x* est un type de mappage   |
| Groupe d’attributs : | eval/Enable                        |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>\_Domaine de \_ grille \_ Map1 GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | points de terminaison de grille 1D                                                             |
| Groupe d’attributs : | eval                                                                           |
| Valeur initiale :   | 0,1                                                                            |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>\_Domaine de \_ grille \_ map2 GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | points de terminaison de grille 2D                                                             |
| Groupe d’attributs : | eval                                                                           |
| Valeur initiale :   | 0, 1 ; 0, 1                                                                     |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>\_Segments de \_ grille \_ Map1 GL</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | divisions de grille 1D                 |
| Groupe d’attributs : | eval                               |
| Valeur initiale :   | 1                                  |
| Commande d’extraction :     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>\_Segments de \_ grille \_ Map1 GL</dt> <dd> 

| Propriété | Valeur |
|------------------|--------------------------------------------------------------------------------|
| Description :     | segments de grille 2D                                                              |
| Groupe d’attributs : | eval                                                                           |
| Valeur initiale :   | 1, 1                                                                           |
| Commande d’extraction :     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>\_standard GL Auto \_</dt> <dd> 

| Propriété | Valeur |
|------------------|---------------------------------------------|
| Description :     | True si la génération automatique normale est activée |
| Groupe d’attributs : | eval                                        |
| Valeur initiale :   | GL- \_ faux                                   |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




