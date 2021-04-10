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
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942892"
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



 

## <a name="remarks"></a>Notes

Les chaînes doivent être localisées en fonction de l’ID de langue du thread appelant.

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

 

 





