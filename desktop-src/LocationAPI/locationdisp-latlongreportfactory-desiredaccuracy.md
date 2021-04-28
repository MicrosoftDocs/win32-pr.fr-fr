---
description: 'Propriété LocationDisp. LatLongReportFactory. DesiredAccuracy : valeur actuelle de précision souhaitée.'
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: LocationDisp. LatLongReportFactory. DesiredAccuracy, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: afc5ec235df6c9e07a665410cb09e00f24305304
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088967"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a>LocationDisp. LatLongReportFactory. DesiredAccuracy, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Valeur actuelle de précision souhaitée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est en lecture/écriture **ULong**.



| Valeur                                                                        | Signification                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Par défaut. Le capteur doit utiliser la précision pour laquelle il peut optimiser l’utilisation de l’alimentation et d’autres considérations relatives aux coûts.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Le capteur doit fournir le rapport le plus précis possible. Cela inclut l'utilisation des services qui peuvent facturer des sommes d'argent ou la consommation de niveaux supérieurs d'alimentation de batterie ou de bande passante de connexion.<br/> |



 

## <a name="remarks"></a>Notes 

Cette valeur est une demande au fournisseur de localisation. Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous avez demandé. Lisez la valeur de cette propriété pour découvrir le paramètre d’intervalle de rapport réel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

