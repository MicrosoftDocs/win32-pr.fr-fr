---
description: Gère les rapports d’adresse postale.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: LocationDisp. CivicAddressReportFactory, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: e6e0efcc63d0d14934abe1f6be1444bf5b7eeaed2bfa0b0cd46efefed3f1bba6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117993021"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>LocationDisp. CivicAddressReportFactory, objet

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Gère les rapports d’adresse postale.

## <a name="members"></a>Membres

L’objet **LocationDisp. CivicAddressReportFactory** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **LocationDisp. CivicAddressReportFactory** possède les méthodes suivantes.



| Méthode                                                                                            | Description                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Demande les événements de rapport d’adresse postale.<br/>                                              |
| [**RequestPermissions**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.<br/> |
| [**StopListeningForReports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Annule les demandes d’événements de rapport d’adresse postale.<br/>                                       |



 

### <a name="properties"></a>Propriétés

L’objet **LocationDisp. CivicAddressReportFactory** possède ces propriétés.



| Propriété                                                                                        | Type d’accès           | Description                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Lecture seule<br/>  | [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md)actuel.<br/> |
| [**DesiredAccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Lecture/écriture<br/> | Paramètre de précision souhaité.<br/>                                                           |
| [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Lecture/écriture<br/> | Intervalle d’événements de rapport d’adresse postale actuel, en millisecondes.<br/>                                |
| [**État**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Lecture seule<br/>  | État actuel du rapport.<br/>                                                                      |



 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment créer cet objet dans du code HTML.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



l’exemple de code suivant montre comment créer cet objet dans JScript à l’aide de Windows Script Host.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



l’exemple de code suivant montre comment créer cet objet dans VBScript à l’aide de Windows Script Host.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LocationDisp.CivicAddressReport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

