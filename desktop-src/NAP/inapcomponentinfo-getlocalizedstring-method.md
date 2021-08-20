---
title: Méthode INapComponentInfo GetLocalizedString (NapCommon. h)
description: Est utilisé par le système NAP pour récupérer les chaînes localisées.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Méthode GetLocalizedString NAP
- Méthode GetLocalizedString NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be55595bf6c5af6e435d9c53c9b473a721005699da494319ba55eaa828da2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134362"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>INapComponentInfo :: GetLocalizedString, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapComponentInfo :: GetLocalizedString** est utilisée par le système NAP pour récupérer les chaînes localisées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ID* \[ de la dans\]
</dt> <dd>

[**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la chaîne à localiser.

</dd> <dt>

*chaîne* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version localisée du message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Les chaînes doivent être localisées en fonction de l’ID de langue du thread appelant.

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

 

 





