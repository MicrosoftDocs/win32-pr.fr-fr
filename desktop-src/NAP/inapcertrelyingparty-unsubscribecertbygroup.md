---
title: Méthode INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Annule l’abonnement à un serveur de certificat d’intégrité (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- Méthode UnSubscribeCertByGroup NAP
- Méthode UnSubscribeCertByGroup NAP, interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, méthode UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942270"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a>INapCertRelyingParty :: UnSubscribeCertByGroup, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **UnSubscribeCertByGroup** se désabonne d’un serveur de certificat d’intégrité (HCS).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 *ID* \[ dans\]
</dt> <dd>

[**EnforcementEntityId**](nap-datatypes.md) qui contient l’ID du client de mise en œuvre qui annule l’abonnement.

</dd> <dt>

 *réservé* \[ dans\]
</dt> <dd>

Doit avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

S’il n’y a pas d’autres abonnés à HCS, NapAgent supprimera les certificats d’intégrité correspondants du magasin de l’ordinateur local.

Avant d’appeler cette méthode, appelez [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).

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

 

 





