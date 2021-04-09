---
description: Gère les rapports de latitude/longitude.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: LocationDisp. LatLongReportFactory, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868893"
---
# <a name="locationdisplatlongreportfactory-object"></a>LocationDisp. LatLongReportFactory, objet

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Gère les rapports de latitude/longitude.

## <a name="members"></a>Membres

L’objet **LocationDisp. LatLongReportFactory** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **LocationDisp. LatLongReportFactory** possède les méthodes suivantes.



| Méthode                                                                                       | Description                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-latlongreportfactory-listenforreports.md)               | Demande des événements de rapport Latitude/Longitude.<br/>                                         |
| [**RequestPermissions**](locationdisp-latlongreportfactory-requestpermissions.md)           | Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.<br/> |
| [**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Annule les demandes d’événements de rapport Latitude/Longitude.<br/>                             |



 

### <a name="properties"></a>Propriétés

L’objet **LocationDisp. LatLongReportFactory** possède ces propriétés.



| Propriété                                                                                | Type d’accès           | Description                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**DesiredAccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Lecture/écriture<br/> | Valeur actuelle de précision souhaitée.<br/>                                                   |
| [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Lecture seule<br/>  | [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md)actuel.<br/> |
| [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Lecture/écriture<br/> | Intervalle d’événements de rapport Latitude/Longitude actuel en millisecondes.<br/>                 |
| [**Statu**](locationdisp-latlongreportfactory-status.md)<br/>                   | Lecture seule<br/>  | État actuel du rapport.<br/>                                                            |



 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment créer cet objet dans du code HTML.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



L’exemple de code suivant montre comment créer cet objet dans JScript à l’aide de Windows Script Host.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



L’exemple de code suivant montre comment créer cet objet dans VBScript à l’aide de Windows Script Host.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

