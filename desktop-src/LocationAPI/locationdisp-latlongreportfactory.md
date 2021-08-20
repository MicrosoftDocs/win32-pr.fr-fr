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
ms.openlocfilehash: 18f8fddd675cc25a78deaf9acf46c41c3d002a4ba394288116020c0d5241d903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809546"
---
# <a name="locationdisplatlongreportfactory-object"></a>LocationDisp. LatLongReportFactory, objet

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

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
| [**État**](locationdisp-latlongreportfactory-status.md)<br/>                   | Lecture seule<br/>  | État actuel du rapport.<br/>                                                            |



 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment créer cet objet dans du code HTML.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



l’exemple de code suivant montre comment créer cet objet dans JScript à l’aide de Windows Script Host.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



l’exemple de code suivant montre comment créer cet objet dans VBScript à l’aide de Windows Script Host.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

