---
title: INapComponentInfo GetDescription, méthode (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir la description d’un client d’intégrité.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- GetDescription, méthode NAP
- GetDescription, méthode NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, GetDescription, méthode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ece376dc2d5c8eb896850e6e92cb6cbd2439bf9b971302b52905368ded575d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891299"
---
# <a name="inapcomponentinfogetdescription-method"></a>INapComponentInfo :: GetDescription, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapComponentInfo :: GetDescription** est utilisée par le système NAP pour obtenir la description d’un client d’intégrité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Description* \[ à\]
</dt> <dd>

Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la description.

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





