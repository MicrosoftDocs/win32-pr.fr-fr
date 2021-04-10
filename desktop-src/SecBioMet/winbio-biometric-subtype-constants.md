---
title: Constantes WINBIO_BIOMETRIC_SUBTYPE ( \_ types WINBIO. h)
description: Fournissez des informations sur une mesure biométrique.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942350"
---
# <a name="winbio_biometric_subtype-constants"></a>\_Constantes de sous-type biométrique WINBIO \_

**WINBIO \_ Les constantes de \_ sous-type BIOmétriques** sont utilisées dans l’Windows Biometric Framework pour fournir des informations supplémentaires sur une mesure biométrique. Les constantes suivantes peuvent être utilisées quand aucun sous-type n’est requis ou lorsqu’un sous-type est requis.



| Constante/valeur                                                                                                                                                                                                                                                            | Description                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ SubType \_ no \_ information**</dt> <dt>0x00</dt> </dl> | Aucune information de sous-type.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ SOUS-TYPE \_ n’importe quel**</dt> <dt>0xFF</dt> </dl>                                   | Tout sous-type.<br/>            |



## <a name="remarks"></a>Notes

Pour rechercher les sous-types biométriques disponibles pour un type biométrique particulier, utilisez le tableau suivant :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur <strong>WINBIO_BIOMETRIC_TYPE</strong></th>
<th>Rubrique (s) pour rechercher <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> valeurs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>Constantes WINBIO_ANSI_385_FACE</strong></a>
<blockquote>
[!Note]<br />
Ces valeurs s’appliquent uniquement à Windows 10 et versions ultérieures.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Une des rubriques suivantes :
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>Constantes WINBIO_ANSI_381_FORMAT</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>Constantes WINBIO_ANSI_381_IMG</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>Constantes WINBIO_ANSI_381_IMG_ACQ</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>Constantes WINBIO_ANSI_381_IMP_TYPE</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>Constantes WINBIO_ANSI_381_PIXELS</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS les constantes d’empreinte digitale</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Constantes WINBIO_ANSI_381_POS_Palm</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>Constantes WINBIO_IRIS</strong></a>
<blockquote>
[!Note]<br />
Ces valeurs s’appliquent uniquement à Windows 10 et versions ultérieures.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Constantes WINBIO_VOICE</strong></a>
<blockquote>
[!Note]<br />
Ces valeurs s’appliquent uniquement à Windows 10 et versions ultérieures.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Pour plus d’informations, consultez [constantes d’application cliente](client-application-constants.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



 

 





