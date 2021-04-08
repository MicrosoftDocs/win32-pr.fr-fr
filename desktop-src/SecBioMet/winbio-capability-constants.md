---
title: Constantes WINBIO_CAPABILITY ( \_ types WINBIO. h)
description: Sous-types de capteur d’empreintes digitales.
ms.assetid: D447273E-2A02-484E-B0E4-69FEADD15797
topic_type:
- apiref
api_name:
- WINBIO_CAPABILITY_SENSOR
- WINBIO_CAPABILITY_MATCHING
- WINBIO_CAPABILITY_DATABASE
- WINBIO_CAPABILITY_PROCESSING
- WINBIO_CAPABILITY_ENCRYPTION
- WINBIO_CAPABILITY_NAVIGATION
- WINBIO_CAPABILITY_INDICATOR
- WINBIO_CAPABILITY_VIRTUAL_SENSOR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16de3f496e5c3723722bb7aae22c81eb27c968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843621"
---
# <a name="winbio_capability-constants"></a>\_Constantes de capacité WINBIO

Les sous-types de capteur d’empreintes suivants sont des valeurs de **\_ fonctionnalités WINBIO** qui peuvent être utilisées comme masque de masque pour le paramètre *Capabilities* de la structure de [**\_ \_ schéma d’unité WINBIO**](winbio-unit-schema.md) . Ils font référence aux fonctionnalités de capteur intégrées.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_SENSOR"></span><span id="winbio_capability_sensor"></span><dl> <dt><strong>WINBIO_CAPABILITY_SENSOR</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Le capteur peut capturer des données biométriques.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_MATCHING"></span><span id="winbio_capability_matching"></span><dl> <dt><strong>WINBIO_CAPABILITY_MATCHING</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Le capteur peut faire correspondre des données biométriques à une identité.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_DATABASE"></span><span id="winbio_capability_database"></span><dl> <dt><strong>WINBIO_CAPABILITY_DATABASE</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Le capteur contient une base de données intégrée.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_PROCESSING"></span><span id="winbio_capability_processing"></span><dl> <dt><strong>WINBIO_CAPABILITY_PROCESSING</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">Le capteur peut effectuer un traitement biométrique.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_ENCRYPTION"></span><span id="winbio_capability_encryption"></span><dl> <dt><strong>WINBIO_CAPABILITY_ENCRYPTION</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">Le capteur peut chiffrer les données biométriques.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_NAVIGATION"></span><span id="winbio_capability_navigation"></span><dl> <dt><strong>WINBIO_CAPABILITY_NAVIGATION</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">Le capteur peut agir comme un tapis de souris. Non pris en charge actuellement.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_INDICATOR"></span><span id="winbio_capability_indicator"></span><dl> <dt><strong>WINBIO_CAPABILITY_INDICATOR</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">Le capteur contient un voyant lumineux.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WINBIO_CAPABILITY_VIRTUAL_SENSOR"></span><span id="winbio_capability_virtual_sensor"></span><dl> <dt><strong>WINBIO_CAPABILITY_VIRTUAL_SENSOR</strong></dt> <dt>0x00000080</dt> </dl></td>
<td style="text-align: left;">L’adaptateur de capteur gère sa propre connexion au matériel biométrique.<br/>
<blockquote>
[!Note]<br />
Cette constante s’applique uniquement à Windows 10 et versions ultérieures.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                                                                                  |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> <dt>

[**\_schéma d’unité WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





