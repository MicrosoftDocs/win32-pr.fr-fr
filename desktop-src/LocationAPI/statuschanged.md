---
description: Se produit lorsque l’état opérationnel d’un rapport change.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Événement StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1d1babe150920bb587d24b0b16be0cf662feba252b2b38bc05dc53e3670dd49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067929"
---
# <a name="statuschanged-event"></a>Événement StatusChanged

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l' [**Windows. API Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

Se produit lorsque l’état opérationnel d’un rapport change.

## <a name="syntax"></a>Syntaxe


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*statut* 
</dt> <dd>

Nouvel état.



| Statut                                                                                               | Signification                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**entre**</dt> </dl> | Rapport non pris en charge.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erreur.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Accès refusé.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Initialisation en cours.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | En cours d'exécution.<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Vous devez implémenter des gestionnaires de rapports de modification d’État distincts pour les rapports d’adresse civique et les rapports de latitude/longitude.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cet événement, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

