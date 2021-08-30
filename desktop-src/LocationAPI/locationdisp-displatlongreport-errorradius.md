---
description: Distance à partir de l’emplacement indiqué, en mètres. Combiné avec l’emplacement signalé comme origine, ce rayon décrit le cercle dans lequel l’emplacement réel est probablement situé.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: LocationDisp. DispLatLongReport. ErrorRadius, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6e331d6001acbdbb7aa97689fdda272a55227f202e8a28c6ba77b56357465dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129999"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a>LocationDisp. DispLatLongReport. ErrorRadius, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Distance à partir de l’emplacement indiqué, en mètres. Combiné avec l’emplacement signalé comme origine, ce rayon décrit le cercle dans lequel l’emplacement réel est probablement situé.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

