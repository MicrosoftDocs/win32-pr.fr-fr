---
title: Styles étendus du contrôle d’édition (CommCtrl. h)
description: Cette section répertorie les styles étendus utilisés lors de la création de contrôles d’édition. La valeur des styles étendus est une combinaison d’opérations de bits de ces styles.
ms.assetid: 44ef7cbf-6d90-4ea0-8e23-cd84aacd5506
topic_type:
- apiref
api_name:
- ES_EX_ALLOWEOL_CR
- ES_EX_ALLOWEOL_LF
- ES_EX_ALLOWEOL_ALL
- ES_EX_CONVERT_EOL_ON_PASTE
- ES_EX_ZOOMABLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 912a13b0e05d7b12e5058435221b821b50eddf2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520890"
---
# <a name="edit-control-extended-styles"></a>Styles étendus du contrôle d’édition

Cette section répertorie les styles étendus utilisés lors de la création de contrôles d’édition. La valeur des styles étendus est une combinaison d’opérations de bits de ces styles.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_CR"></span><span id="es_ex_alloweol_cr"></span><dl> <dt><strong>ES_EX_ALLOWEOL_CR</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista et versions ultérieures](common-control-versions.md). Active la prise en charge des caractères de fin de ligne de retour chariot (CR) pour couper les lignes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_LF"></span><span id="es_ex_alloweol_lf"></span><dl> <dt><strong>ES_EX_ALLOWEOL_LF</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista et versions ultérieures](common-control-versions.md). Active la prise en charge des caractères de fin de ligne (LF) pour les sauts de ligne.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ALLOWEOL_ALL"></span><span id="es_ex_alloweol_all"></span><dl> <dt><strong>ES_EX_ALLOWEOL_ALL</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista et versions ultérieures](common-control-versions.md). Active la prise en charge des caractères de fin de retour chariot (CR) et de saut de ligne (LF) sur les lignes de séparation.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_EX_CONVERT_EOL_ON_PASTE"></span><span id="es_ex_convert_eol_on_paste"></span><dl> <dt><strong>ES_EX_CONVERT_EOL_ON_PASTE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista et versions ultérieures](common-control-versions.md). Convertit les caractères de fin de ligne activés pour ce contrôle d’édition dans le contenu collé pour qu’ils correspondent au caractère de fin de ligne utilisé par le document actif.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_EX_ZOOMABLE"></span><span id="es_ex_zoomable"></span><dl> <dt><strong>ES_EX_ZOOMABLE</strong></dt> </dl></td>
<td style="text-align: left;">[Windows Vista et versions ultérieures](common-control-versions.md). Active le zoom à l’aide de Ctrl + MouseWheel et des messages [**em \_ GETZOOM**](em-getzoom.md) / [**em \_ SETZOOM**](em-setzoom.md) .<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





