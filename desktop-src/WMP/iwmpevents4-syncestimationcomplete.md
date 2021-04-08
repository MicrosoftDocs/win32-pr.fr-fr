---
title: Méthode IWMPEvents4 SyncEstimationComplete
description: L’événement SyncEstimationComplete se produit lorsqu’une estimation de la taille, précédemment lancée par IWMPSyncDevice3 estimateSyncSize, est terminée.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Méthode SyncEstimationComplete lecteur Windows Media
- Méthode SyncEstimationComplete lecteur Windows Media, interface IWMPEvents4
- Interface IWMPEvents4 lecteur Windows Media, méthode SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723386"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>IWMPEvents4 :: SyncEstimationComplete, méthode

L’événement **SyncEstimationComplete** se produit lorsqu’une estimation de la taille, précédemment lancée par [**IWMPSyncDevice3 :: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), est terminée.

## <a name="syntax"></a>Syntaxe


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) qui représente l’appareil pour lequel l’estimation de la taille a été initiée.

</dd> <dt>

*hrResult* \[ dans\]
</dt> <dd>

Valeur qui indique la réussite ou l’échec de l’estimation.



| Valeur                                                                                                                                       | Signification                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_OK**</dt> </dl>          | Estimation réussie.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**E \_ Abort**</dt> </dl> | L’estimation a été abandonnée.<br/> |



 

</dd> <dt>

*lEstimatedUsedSpace* \[ dans\]
</dt> <dd>

Espace estimé (en octets) qui doit être utilisé sur l’appareil.

</dd> <dt>

*lEstimatedSize* \[ dans\]
</dt> <dd>

Taille estimée (en octets) des données à synchroniser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





