---
description: Représente un rapport de latitude/longitude.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: LocationDisp. DispLatLongReport, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535618"
---
# <a name="locationdispdisplatlongreport-object"></a>LocationDisp. DispLatLongReport, objet

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Représente un rapport de latitude/longitude.

## <a name="members"></a>Membres

L’objet **LocationDisp. DispLatLongReport** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **LocationDisp. DispLatLongReport** possède ces propriétés.



| Propriété                                                                         | Type d’accès          | Description                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Altitude**](locationdisp-displatlongreport-altitude.md)<br/>           | Lecture seule<br/> | Altitude actuelle, en mètres.<br/>                                                                                                                                                           |
| [**AltitudeError**](locationdisp-displatlongreport-altitudeerror.md)<br/> | Lecture seule<br/> | Erreur d’altitude, en mètres.<br/>                                                                                                                                                             |
| [**ErrorRadius**](locationdisp-displatlongreport-errorradius.md)<br/>     | Lecture seule<br/> | Distance à partir de l’emplacement indiqué, en mètres. Combiné avec l’emplacement signalé comme origine, ce rayon décrit le cercle dans lequel l’emplacement réel est proably.<br/> |
| [**Latitude**](locationdisp-displatlongreport-latitude.md)<br/>           | Lecture seule<br/> | Latitude actuelle, en degrés.<br/>                                                                                                                                                          |
| [**Longitude**](locationdisp-displatlongreport-longitude.md)<br/>         | Lecture seule<br/> | Longitude actuelle, en degrés.<br/>                                                                                                                                                         |
| [**Timestamp**](locationdisp-displatlongreport-timestamp.md)<br/>         | Lecture seule<br/> | Date et heure de génération du rapport.<br/>                                                                                                                                       |



 

## <a name="remarks"></a>Notes

Vous pouvez récupérer cet objet via la propriété [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) de l’objet [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) . Vous pouvez recevoir cet objet via l’événement [**NewLatLongReport**](newlatlongreport.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

