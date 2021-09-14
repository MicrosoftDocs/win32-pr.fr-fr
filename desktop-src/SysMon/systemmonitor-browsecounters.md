---
title: Méthode SystemMonitor BrowseCounters
description: Affiche la boîte de dialogue Ajouter des compteurs.
ms.assetid: 7edc4a80-4a04-49fd-b383-b892e1e16215
keywords:
- Méthode BrowseCounters SysMon
- Méthode BrowseCounters SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, méthode BrowseCounters
topic_type:
- apiref
api_name:
- SystemMonitor.BrowseCounters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96df5d50ab9fc89963f9d09f4c0cb92479b4ecac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008829"
---
# <a name="systemmonitorbrowsecounters-method"></a>SystemMonitor :: BrowseCounters, méthode

Affiche la boîte de dialogue **Ajouter des compteurs** .

## <a name="syntax"></a>Syntaxe


```VB
Sub BrowseCounters()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette boîte de dialogue permet à l’utilisateur de sélectionner des compteurs de performance locaux ou distants dans une liste d’objets de performance. Les compteurs sélectionnés sont ajoutés à la collection de [**compteurs**](counters.md) et s’affichent dans le graphique ou le rapport.

Pour recevoir une notification lorsqu’un compteur est ajouté, implémentez l’événement [**OnCounterAdded**](systemmonitor-oncounteradded.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**Compteurs. Add**](counters-add.md)
</dt> </dl>

 

 





