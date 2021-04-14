---
title: Méthode INapComponentInfo GetVendorName (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir le nom du fournisseur d’un client d’intégrité.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- Méthode GetVendorName NAP
- Méthode GetVendorName NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetVendorName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467070"
---
# <a name="inapcomponentinfogetvendorname-method"></a>INapComponentInfo :: GetVendorName, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapComponentInfo :: GetVendorName** est utilisée par le système NAP pour obtenir le nom du fournisseur d’un client d’intégrité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NomFournisseur* \[ à\]
</dt> <dd>

Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource du nom du fournisseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





