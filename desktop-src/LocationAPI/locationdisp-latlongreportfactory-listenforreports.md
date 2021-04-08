---
description: Demande des événements de rapport Latitude/Longitude.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Méthode LocationDisp. LatLongReportFactory. ListenForReports (Locationapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757336"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a>Méthode LocationDisp. LatLongReportFactory. ListenForReports

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Demande des événements de rapport Latitude/Longitude.

## <a name="syntax"></a>Syntaxe


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*requestedReportInterval* 
</dt> <dd> Nombre (**double mot**) représentant le délai demandé entre les événements de rapport Latitude/Longitude, en millisecondes. Consultez la section Notes.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le fournisseur d’emplacement n’est pas obligé de fournir des rapports à l’intervalle que vous demandez. Lisez la valeur de la propriété [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) pour découvrir le paramètre d’intervalle de rapport réel.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| En-tête<br/>                   | <dl> <dt>Locationapi. h</dt> </dl> |



 

