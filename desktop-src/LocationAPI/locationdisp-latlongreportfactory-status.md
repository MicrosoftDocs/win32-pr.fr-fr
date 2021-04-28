---
description: 'Propriété LocationDisp. LatLongReportFactory. Status : état actuel du rapport.'
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: LocationDisp. LatLongReportFactory. Status, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 37e66c3f289f5376b31ffe516f45d79f2fef51e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088897"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a>LocationDisp. LatLongReportFactory. Status, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

État actuel du rapport.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est un **nombre** en lecture seule (unsigned long).



| Statut                                                                                               | Signification                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Rapport non pris en charge.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erreur.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Accès refusé.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Initialisation en cours.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | En cours d'exécution.<br/>              |



 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette propriété, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

