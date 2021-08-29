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
ms.openlocfilehash: 4e9d94fd0816e9e8b3e89ba4001b30d83617276938c683f8f0efb6fd17530cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891445"
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



 

## <a name="remarks"></a>Remarques

L’appelant doit libérer le paramètre *relyingParties* à l’aide de **CoTaskMemFree**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                               |
| En-tête<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapCertRelyingParty**](inapcertrelyingparty.md)
</dt> </dl>

 

 





