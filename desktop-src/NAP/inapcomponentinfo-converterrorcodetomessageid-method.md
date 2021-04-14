---
title: Méthode INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: Est utilisé par le système NAP pour demander au client d’intégrité de convertir un code d’erreur HRESULT en ID de message.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Méthode ConvertErrorCodeToMessageId NAP
- Méthode ConvertErrorCodeToMessageId NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466775"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>INapComponentInfo :: ConvertErrorCodeToMessageId, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode de rappel **INapComponentInfo :: ConvertErrorCodeToMessageId** est utilisée par le système NAP pour demander au client d’intégrité de convertir un code d’erreur HRESULT en ID de message.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ErrorCode* \[ dans\]
</dt> <dd>

[**Code d’erreur**](nap-error-constants.md) du système NAP qui doit être converti en **MessageID**.

</dd> <dt>

*ID* \[ de la à\]
</dt> <dd>

Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la chaîne localisée correspondante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

Le **MessageID** retourné est utilisé par le système NAP pour récupérer une chaîne localisée.

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

 

 





