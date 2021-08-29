---
title: Méthode INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: S’abonne à un serveur de certificat d’intégrité (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- Méthode SubscribeCertByGroup NAP
- Méthode SubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, méthode SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a8ed7f7dd97bf77e99e493a7c0521c62fcbcaaa776a364d0fe7e322e056de5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891441"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a>INapCertRelyingParty :: SubscribeCertByGroup, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **SubscribeCertByGroup** s’abonne à un serveur de certificat d’intégrité (HCS). Le HCS doit déjà être inscrit avant l’abonnement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 *ID* \[ dans\]
</dt> <dd>

[**EnforcementEntityId**](nap-datatypes.md) qui contient l’ID du client de mise en œuvre qui s’abonne.

</dd> <dt>

*SubscriberName* \[ dans\]
</dt> <dd>

Nom de l'abonné.

> [!Note]  
> Actuellement utilisé uniquement à des fins de journalisation.

 

</dd> <dt>

*réservé* \[ dans\]
</dt> <dd>

Doit avoir la **valeur null**.

</dd> <dt>

*certExists* \[ à\]
</dt> <dd>

Indique si un certificat d’intégrité de ce HCS est déjà géré par le NapAgent et s’il est présent dans le magasin de l’ordinateur. Si la **valeur est true**, un certificat d’intégrité est déjà en cours de maintenance et est présent. Si la **valeur est false**, un certificat d’intégrité n’est pas actuellement géré et présent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

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

 

 





