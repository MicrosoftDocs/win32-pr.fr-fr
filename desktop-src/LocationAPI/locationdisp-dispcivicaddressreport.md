---
description: Représente un rapport d’adresse postale.
ms.assetid: 7c6e790f-0150-4ea8-9583-df633ebf035d
title: LocationDisp. DispCivicAddressReport, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5646bd6df1a2523faf481bc867acc67dbd0a647b4cdf3f033d7327a66174d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129979"
---
# <a name="locationdispdispcivicaddressreport-object"></a>LocationDisp. DispCivicAddressReport, objet

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Représente un rapport d’adresse postale.

## <a name="members"></a>Membres

L’objet **LocationDisp. DispCivicAddressReport** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **LocationDisp. DispCivicAddressReport** possède ces propriétés.



| Propriété                                                                              | Type d’accès          | Description                                                 |
|:--------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------|
| [**AddressLine1**](locationdisp-dispcivicaddressreport-addressline1.md)<br/>   | Lecture seule<br/> | Première ligne d’une adresse postale.<br/>              |
| [**AddressLine2**](locationdisp-dispcivicaddressreport-addressline2.md)<br/>   | Lecture seule<br/> | Deuxième ligne d’une adresse postale.<br/>             |
| [**City**](locationdisp-dispcivicaddressreport-city.md)<br/>                   | Lecture seule<br/> | Nom de la ville.<br/>                                   |
| [**Pays**](locationdisp-civicaddressreport-countryregion.md)<br/>     | Lecture seule<br/> | Nom du pays ou de la région.<br/>                      |
| [**DetailLevel**](locationdisp-dispcivicaddressreport-detaillevel.md)<br/>     | Lecture seule<br/> | Niveau de détail du rapport.<br/>                 |
| [**Postal**](locationdisp-dispcivicaddressreport-postalcode.md)<br/>       | Lecture seule<br/> | Le code postal.<br/>                                 |
| [**StateProvince**](locationdisp-dispcivicaddressreport-stateprovince.md)<br/> | Lecture seule<br/> | Nom de l’État ou de la province.<br/>                      |
| [**Timestamp**](locationdisp-dispcivicaddressreport-timestamp.md)<br/>         | Lecture seule<br/> | Date et heure de génération du rapport.<br/> |



 

## <a name="remarks"></a>Remarques

Vous pouvez récupérer cet objet via la propriété [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md) d’un objet [**CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md) . Vous pouvez recevoir cet objet via l’événement [**NewCivicAddressReport**](newcivicaddressreport.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

