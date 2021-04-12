---
title: Méthode INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Obtient une liste des parties de confiance qui sont abonnées.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- Méthode GetSubscribedRelyingParties NAP
- Méthode GetSubscribedRelyingParties NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, méthode GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464490"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a>INapCertRelyingParty :: GetSubscribedRelyingParties, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **GetSubscribedRelyingParties** obtient une liste des parties de confiance qui sont abonnées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ à\]
</dt> <dd>

Pointeur vers un [**EnforcementEntityCount**](nap-datatypes.md) qui contient le nombre de parties de confiance abonnées.

</dd> <dt>

*relyingParties* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un [**EnforcementEntityId**](nap-datatypes.md) qui contient la liste des parties de confiance abonnées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

L’appelant doit libérer le paramètre *relyingParties* à l’aide de **CoTaskMemFree**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                               |
| En-tête<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





