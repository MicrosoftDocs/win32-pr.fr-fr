---
title: Méthode INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator. h)
description: Utilisé par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de configuration dans une demande de validation.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Méthode GetConfigID NAP
- Méthode GetConfigID NAP, interface INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 interface NAP, méthode GetConfigID
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72acdd170726d2d94e4fbc46864a7e5aab6b902d7b1ee25b63ee0fa9e376c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625979"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>INapSystemHealthValidationRequest2 :: GetConfigID, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthValidationRequest2 :: GetConfigId** est utilisée par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de configuration dans une demande de validation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configID* \[ à\]
</dt> <dd>

Au retour, pointeur vers UINT32 qui contient un ID de configuration de la SHV.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | L’opération a réussi.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre configID a la **valeur null**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





