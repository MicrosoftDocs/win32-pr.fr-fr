---
description: Spécifie que le frame actuel est encodé à l’aide d’un ou de plusieurs frames LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749356"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>CODECAPI \_ propriété AVEncVideoUseLTRFrame

Spécifie que le frame actuel est encodé à l’aide d’un ou de plusieurs frames LTR.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Valeur de la propriété

La valeur de ce contrôle inclut deux champs, où chaque champ a 16 bits.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>Les premiers bits de champ</strong></dt> <dt>[0.. 15]</dt> </dl></td>
<td>Indique le ou les frames LTR autorisés pour l’encodage du frame actuel. <br/> <strong>Encodeurs H. 264/AVC :</strong><br/> Il s’agit d’une image bitmap qui indique les cadres LTR qui peuvent être utilisés comme référence pour ce frame. Le bit le moins significatif correspond à l’index LTR 0, le deuxième bit le moins significatif correspond à l’index 1 LTR, etc.<br/> Cette valeur ne doit pas être égale à 0.<br/> L’index le plus élevé spécifié par cette valeur ne doit pas être supérieur au nombre maximal de cadres LTR spécifié dans la propriété <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> moins un.<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Deuxième bits de champ</strong></dt> <dt>[16.. 31]</dt> </dl></td>
<td>Indicateur qui spécifie si des limitations supplémentaires sont requises pour l’encodage des frames suivants. <br/> <strong>Encodeurs H. 264/AVC :</strong><br/> 1 est la seule valeur valide pour ce champ. Toutes les autres valeurs sont non valides et réservées pour une utilisation ultérieure.<br/> Lorsque l’indicateur a la valeur 1, l’encodeur doit encoder les frames suivants dans l’ordre d’encodage selon les contraintes suivantes :<br/>
<ul>
<li>Elle n’utilise pas les frames de référence à long terme dans l’ordre de codage antérieur à l’image actuelle ou l’encodage futur dans l’ordre de codage.</li>
<li>Il ne doit pas utiliser les cadres LTR non décrits par le dernier contrôle de CODECAPI_AVEncVideoUseLTRFrame.</li>
<li>Elle peut utiliser des images LTR mises à jour après le frame actuel.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

**Encodeurs H. 264/AVC :**

Cette propriété ne doit pas être appelée si un appel en attente d’utilisation d’un frame LTR a été émis à l’aide de la \_ propriété CODECAPI AVEncVideoUseLTRFrame et que l’encodeur n’a pas encore généré de frame qui a utilisé le LTR. En d’autres termes, l’encodeur ne doit pas faire remonter les \_ demandes CODECAPI AVEncVideoUseLTRFrame.

Si une \_ demande CODECAPI AVEncVideoUseLTRFrame est soumise alors qu’une autre \_ demande de AVEncVideoUseLTRFrame CODECAPI est toujours en attente, la demande plus ancienne doit être supprimée.

L’appel de CODECAPI \_ AVEncVideoUseLTRFrame sur un frame de couche non-base est valide et s’applique au frame de couche non-base, sans délai, à un frame de couche de base.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




