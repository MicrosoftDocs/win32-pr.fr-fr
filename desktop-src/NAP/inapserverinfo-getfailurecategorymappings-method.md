---
title: Méthode INapServerInfo GetFailureCategoryMappings (NapServerManagement. h)
description: Récupère les mappages de catégorie d’échec pour un SHA ou un VALIDateur spécifié.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Méthode GetFailureCategoryMappings NAP
- Méthode GetFailureCategoryMappings NAP, interface INapServerInfo
- INapServerInfo interface NAP, méthode GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413780"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a>INapServerInfo :: GetFailureCategoryMappings, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapServerInfo :: GetFailureCategoryMappings** récupère les mappages de catégorie d’échec pour un SHA ou un validateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

[**SystemHealthEntityId**](nap-type-constants.md) qui contient l’identificateur unique de l’agent SHA ou du SHV.

</dd> <dt>

*mappage* \[ à\]
</dt> <dd>

Pointeur vers un [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) qui contient les données de mappage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                               |
| En-tête<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





