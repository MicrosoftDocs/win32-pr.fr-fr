---
description: 'Propriété LocationDisp. CivicAddressReportFactory. DesiredAccuracy : valeur actuelle de précision souhaitée.'
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: LocationDisp. CivicAddressReportFactory. DesiredAccuracy, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca2d4f4a7be4afa800cfe81b5df7396be579197e7f997019f4ece3a39598c975
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693129"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a>LocationDisp. CivicAddressReportFactory. DesiredAccuracy, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Valeur actuelle de précision souhaitée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est en lecture/écriture **ULong**.



| Valeur                                                                        | Signification                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Par défaut. Le capteur doit utiliser la précision pour laquelle il peut optimiser l’utilisation de l’alimentation et d’autres considérations relatives aux coûts.<br/>                                                                          |
| <dl> <dt>1</dt> </dl> | Le capteur doit fournir le rapport le plus précis possible. Cela inclut l'utilisation des services qui peuvent facturer des sommes d'argent ou la consommation de niveaux supérieurs d'alimentation de batterie ou de bande passante de connexion.<br/> |



 

## <a name="remarks"></a>Remarques

Cette valeur est une demande au fournisseur de localisation. Le fournisseur de localisation n’est pas requis pour fournir la précision que vous demandez. Lisez la valeur de cette propriété pour découvrir le véritable paramètre de précision.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

