---
description: Intervalle d’événements de rapport d’adresse postale actuel, en millisecondes.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: LocationDisp. CivicAddressReportFactory. ReportInterval, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387160"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>LocationDisp. CivicAddressReportFactory. ReportInterval, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Intervalle d’événements de rapport d’adresse postale actuel, en millisecondes.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est en lecture/écriture **ULong**.

## <a name="remarks"></a>Remarques

Cette valeur est une demande pour le fournisseur de localisation. Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous avez demandé. Lisez la valeur de cette propriété pour découvrir le paramètre d’intervalle de rapport réel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

