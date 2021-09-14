---
title: IWMDRMIndividualizationStatus GetStatus, méthode (wmdrmsdk. h)
description: La méthode GetStatus récupère des informations détaillées sur la progression de l’individualisation.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Méthode GetStatus Windows Media format
- Méthode GetStatus Windows Media format, interface IWMDRMIndividualizationStatus
- Interface IWMDRMIndividualizationStatus Windows Media format, GetStatus, méthode
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293830"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>IWMDRMIndividualizationStatus :: GetStatus, méthode

La méthode **GetStatus** récupère des informations détaillées sur la progression de l’individualisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStatus* \[ à\]
</dt> <dd>

Reçoit une structure d’état de l' [**\_ \_ individualisation WM**](drmwm-individualize-status.md) contenant des informations détaillées sur l’état de la tentative d’individualisation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





