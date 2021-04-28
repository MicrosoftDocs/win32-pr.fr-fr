---
description: 'Propriété LocationDisp. CivicAddressReportFactory. Status : état actuel du rapport.'
ms.assetid: 3aae0b61-cdaa-4131-b6e1-406813bb1848
title: LocationDisp. CivicAddressReportFactory. Status, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: acb5bcfa589139e2c69e75124253f9d9a7b53a87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118497"
---
# <a name="locationdispcivicaddressreportfactorystatus-property"></a>LocationDisp. CivicAddressReportFactory. Status, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

État actuel du rapport.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Status = LocationDisp.CivicAddressReportFactory.Status
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

Pour obtenir un exemple d’utilisation de cette propriété, consultez [écoute des événements de rapport d’adresse postale](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

