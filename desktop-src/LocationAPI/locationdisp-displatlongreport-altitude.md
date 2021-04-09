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
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865478"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a>LocationDisp. DispLatLongReport. altitude, propriété

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Altitude actuelle, en mètres. L’altitude est relative à la référence ellipsoïde.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a>Valeur de la propriété

Cette propriété est un **nombre** en lecture seule (virgule flottante double précision).

## <a name="remarks"></a>Notes

Les capteurs d’emplacement ne sont pas requis pour fournir cette propriété. Vous devez gérer les exceptions lorsque vous tentez d’accéder à cette propriété.

La méthode **altitude** récupère l’altitude relative à la ellipsoïde de référence qui est définie par la dernière révision du système géodésique universel (WGS 84), plutôt que l’altitude par rapport au niveau de la mer.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette propriété, consultez [un exemple de rapport LatLong simple](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

