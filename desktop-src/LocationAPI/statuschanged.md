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
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211101"
---
# <a name="statuschanged-event"></a>Événement StatusChanged

\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]

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
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Rapport non pris en charge.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Erreur.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Accès refusé.<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Initialisation en cours.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | En cours d'exécution.<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Vous devez implémenter des gestionnaires de rapports de modification d’État distincts pour les rapports d’adresse civique et les rapports de latitude/longitude.

## <a name="examples"></a>Exemples

Pour obtenir un exemple d’utilisation de cet événement, consultez [écoute des événements de rapport LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                  |



 

