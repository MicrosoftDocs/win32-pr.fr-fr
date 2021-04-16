---
description: Spécifie le nombre maximal de cadres de référence à long terme (LTR) contrôlés par l’application.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524631"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>CODECAPI \_ propriété AVEncVideoLTRBufferControl

Spécifie le nombre maximal de cadres de référence à long terme (LTR) contrôlés par l’application.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoLTRBufferControl**

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
<td>Nombre de cadres LTR contrôlés par l’application.<br/> <strong>Encodeurs H. 264/AVC :</strong><br/> En supposant que la valeur est N et que N est une valeur différente de zéro, à chaque image de la base de connaissances, l’encodeur doit automatiquement marquer les frames qui suivent la trame de la base de connaissances (et inclure le cadre de la base de demande) comme des cadres LTR, à condition que les 3 des éléments suivants s’appliquent :
<ul>
<li>Le cadre n’est pas déjà défini pour être marqué comme cadre de référence à long terme.</li>
<li>Le cadre est un cadre de couche de base. Par exemple, l’élément de syntaxe <strong>temporal_id</strong> égal à 0.</li>
<li>Le nombre de frames actuellement marqués comme LTR est inférieur à N.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Deuxième bits de champ</strong></dt> <dt>[16.. 31]</dt> </dl></td>
<td>Mode d’approbation du contrôle LTR.<br/> <strong>Encodeurs H. 264/AVC :</strong><br/> 1 (confiance jusqu’à) signifie que l’encodeur peut utiliser un frame LTR, sauf si l’application l’invalide explicitement via le contrôle <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br/> Les autres valeurs ne sont pas valides et réservées pour une utilisation ultérieure.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Il s’agit d’une API statique.

La valeur par défaut doit être 0

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

 

 




