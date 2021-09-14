---
title: Pixel, opérations
description: Pixel, opérations
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Opérations de pixel OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121293"
---
# <a name="pixel-operations"></a>Pixel, opérations

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_test de ciseaux du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Ciseaux activé                 |
| Groupe d’attributs : | ciseaux/activer                     |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_zone de ciseaux du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Zone de ciseaux                                                                      |
| Groupe d’attributs : | ciseaux                                                                          |
| Valeur initiale :   |                                                                                  |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_test du stencil du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Stencil activé                 |
| Groupe d’attributs : | stencil-tampon/activer              |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>\_Func de gabarit GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Fonction de stencil                                                                 |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | \_toujours GL                                                                       |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_masque de \_ valeur du stencil du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Masque du gabarit                                                                     |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | du 1                                                                              |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>Réf. du \_ stencil GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Valeur de référence du stencil                                                          |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | 0                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>\_échec du stencil du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Action d’échec du stencil                                                              |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | conserver le GL \_                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>échec de la profondeur du test de \_ stencil du GL \_ \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Action en cas d’échec du tampon de profondeur du stencil                                                 |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | conserver le GL \_                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>passe de profondeur du test de la \_ passe du gabarit GL \_ \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Action de passe de tampon de profondeur du stencil                                                 |
| Groupe d’attributs : | stencil-tampon                                                                   |
| Valeur initiale :   | conserver le GL \_                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>TEST du GL \_ alpha \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Test alpha activé                 |
| Groupe d’attributs : | mémoire tampon de couleur/activation                |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>\_Func alpha de \_ test \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Fonction de test alpha                                                              |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | \_toujours GL                                                                       |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>Référence de test du GL \_ alpha \_ \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Valeur de référence de test alpha                                                       |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | 0                                                                                |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_test de profondeur du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Mémoire tampon de profondeur activée               |
| Groupe d’attributs : | cache de profondeur/activer                |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_Func de profondeur GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Fonction de test de la mémoire tampon de profondeur                                                       |
| Groupe d’attributs : | mémoire tampon de profondeur                                                                     |
| Valeur initiale :   | GL \_ moins                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>fusion du GL \_</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Fusion activée                   |
| Groupe d’attributs : | mémoire tampon de couleur/activation                |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_BLENC \_ source GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Fusion de la fonction source                                                         |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | GL \_ 1                                                                          |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>heure d’été du GL de \_ fusion \_</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Fusion de la fonction destination                                                    |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | \_zéro GL                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>\_tramage GL</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Tramage activé                  |
| Groupe d’attributs : | mémoire tampon de couleur/activation                |
| Valeur initiale :   | GL \_ true                           |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ logique \_ op</dt> <dd> 

| Propriété | Valeur |
|------------------|------------------------------------|
| Description :     | Opération logique activée          |
| Groupe d’attributs : | mémoire tampon de couleur/activation                |
| Valeur initiale :   | GL- \_ faux                          |
| Commande d’extraction :     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_mode logique \_ du \_ GL</dt> <dd> 

| Propriété | Valeur |
|------------------|----------------------------------------------------------------------------------|
| Description :     | Fonction d’opération logique                                                       |
| Groupe d’attributs : | mémoire tampon de couleur                                                                     |
| Valeur initiale :   | \_copie GL                                                                         |
| Commande d’extraction :     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




