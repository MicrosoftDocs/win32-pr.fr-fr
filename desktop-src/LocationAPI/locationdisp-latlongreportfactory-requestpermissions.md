---
description: 'Méthode LocationDisp. LatLongReportFactory. RequestPermissions : ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.'
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: Méthode LocationDisp. LatLongReportFactory. RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ffbae03d22cee89b5974b32b224c779210e82feb23292628a5a705bc203dbc5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129829"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>Méthode LocationDisp. LatLongReportFactory. RequestPermissions

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.

## <a name="syntax"></a>Syntaxe


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hWnd* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

L’appel est synchrone et l’appelant attend la fermeture de la boîte de dialogue.

> [!Note]  
> si une application s’exécutant en mode protégé, telle qu’un objet d’assistance du navigateur (BHO) pour Internet Explorer, appelle **RequestPermissions** et que l’utilisateur choisit l’option **ne pas activer ce capteur d’emplacement** dans la boîte de dialogue, le fournisseur de localisation n’est pas activé, mais Windows affiche à nouveau la boîte de dialogue si **RequestPermissions** est appelé de nouveau par le même utilisateur. Les applications qui s’exécutent en mode protégé peuvent choisir de ne pas appeler **RequestPermissions** au démarrage, de sorte que l’utilisateur ne voit pas une boîte de dialogue éventuellement indésirable à chaque démarrage de l’application.

 

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cette méthode, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

