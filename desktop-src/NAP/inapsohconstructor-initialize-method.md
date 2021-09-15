---
title: INapSoHConstructor Initialize, méthode (NapProtocol. h)
description: Initialise un paquet de protocole SoH dans le système NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413761"
---
# <a name="inapsohconstructorinitialize-method"></a>INapSoHConstructor :: Initialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHConstructor :: Initialize** Initialise un paquet de protocole SOH dans le système NAP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ dans\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent SHA ou SHV qui construit le paquet.

</dd> <dt>

*isRequest* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui est **true** si le paquet doit être un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** s’il doit s’agir d’un **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L’opération a réussi.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode doit être appelée exactement une fois par paquet.

Le [SystemHealthEntityId](nap-datatypes.md) spécifié dans *ID*, est le premier TLV dans le paquet SOH nouvellement construit et a le type d’attribut [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





