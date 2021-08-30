---
description: Se produit lors de la génération d’un rapport de latitude/longitude.
ms.assetid: 2b1a25a1-ccd6-43f8-979b-c2d414d666a2
title: Événement NewLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3cc8a46267927aaf7bf3011acbd05a32244fd0dcd8cc354a2bde1a299aaca624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129799"
---
# <a name="newlatlongreport-event"></a>Événement NewLatLongReport

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Se produit lors de la génération d’un rapport de latitude/longitude.

## <a name="syntax"></a>Syntaxe


```JScript
.NewLatLongReport(
  newReport
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newReport* 
</dt> <dd>

Nouvel objet [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cet événement, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

