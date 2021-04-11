---
description: Intervalle d’événements de rapport Latitude/Longitude actuel en millisecondes.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: LocationDisp. LatLongReportFactory. ReportInterval, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203410"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>LocationDisp. LatLongReportFactory. ReportInterval, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Intervalle d’événements de rapport Latitude/Longitude actuel en millisecondes.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est en lecture/écriture **ULong**.

## <a name="remarks"></a>Notes

Cette valeur est une demande au fournisseur de localisation. Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous demandez. Lisez la valeur de cette propriété pour découvrir le paramètre d’intervalle de rapport réel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

