---
description: Date et heure de génération du rapport.
ms.assetid: b9435384-72e0-42c4-a948-df52621a5ec2
title: LocationDisp. DispCivicAddressReport. Timestamp, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b805454a6c2d62a58ba5a2a3de8f5b5095e1db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518912"
---
# <a name="locationdispdispcivicaddressreporttimestamp-property"></a>LocationDisp. DispCivicAddressReport. Timestamp, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Date et heure de génération du rapport.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Timestamp = LocationDisp.DispCivicAddressReport.Timestamp
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est une **Date** en lecture seule. Les horodatages sont fournis comme temps universel coordonné (UTC, Universal Time Coordinated).

## <a name="remarks"></a>Notes

Notez que les langages de script, tels que Microsoft JScript, peuvent vous obliger à effectuer des conversions dans d’autres formats d’heure lorsque vous affichez des horodatages sous forme de chaînes.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport d’adresse postale simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

