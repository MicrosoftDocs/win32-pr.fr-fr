---
title: Méthode INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Utilisé par l’agent NAP pour interroger les programmes de validation d’intégrité système (SHV) installés sur le client.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Méthode GetInstalledShvs NAP
- Méthode GetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40cb18f749adc9a1b7003a777cc821fb5e003b83322a7d54c2efda4b8e5739f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939640"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a>INapEnforcementClientConnection2 :: GetInstalledShvs, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetInstalledShvs** est utilisée par l’agent NAP pour interroger les programmes de validation d’intégrité système (SHV) installés sur le client.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ à\]
</dt> <dd>

Pointeur vers une valeur [SystemHealthEntityCount](nap-datatypes.md) qui spécifie le nombre de validateurs d’intégrité du système installés dans *IDS*.

</dd> <dt>

*ID* \[ à\]
</dt> <dd>

Pointeur vers un tableau de valeurs [SystemHealthEntityId](nap-datatypes.md) qui contiennent les ID SHV installés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                   | Description                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Opération réussie.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un argument non valide a été passé à la méthode.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





