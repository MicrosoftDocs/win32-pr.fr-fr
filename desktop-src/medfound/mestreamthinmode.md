---
description: Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux. Pour plus d’informations sur la réduction, consultez à propos du contrôle du taux.
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: Événement MEStreamThinMode (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e19d25e5ab0430d96a9d431c941288e260092b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519602"
---
# <a name="mestreamthinmode-event"></a>Événement MEStreamThinMode

Déclenché par un flux multimédia lorsqu’il démarre ou arrête l’affinage du flux. Pour plus d' *informations sur la réduction, consultez* [à propos du contrôle du taux](about-rate-control.md).

Cet événement peut être envoyé en réponse à la méthode [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) seou à la méthode [**IMFQualityAdvise :: SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) .

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL<br/></td>
<td>Indique si l’affinage a démarré ou s’est arrêté.<br/>
<ul>
<li>VARIANT_TRUE : les exemples fournis après cet événement sont éclaircis.</li>
<li>VARIANT_FALSE : les exemples fournis après cet événement ne sont pas éclaircis.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




