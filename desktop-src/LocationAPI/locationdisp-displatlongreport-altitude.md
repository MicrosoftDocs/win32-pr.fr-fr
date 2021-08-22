---
description: Altitude actuelle, en mètres. L’altitude est relative à la référence ellipsoïde.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. DispLatLongReport. altitude, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8ee6c2cd4257d7f7db97b89a5af4603f5c5129b7f07fe9bfbe6444bb9d347422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067939"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>LocationDisp. DispLatLongReport. altitude, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Altitude actuelle, en mètres. L’altitude est relative à la référence ellipsoïde.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).

## <a name="remarks"></a>Remarques

Les capteurs d’emplacement ne sont pas requis pour fournir cette propriété. Vous devez gérer les exceptions lorsque vous tentez d’accéder à cette propriété.

La méthode **altitude** récupère l’altitude relative à la ellipsoïde de référence qui est définie par la dernière révision du système géodésique universel (WGS 84), plutôt que l’altitude par rapport au niveau de la mer.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

