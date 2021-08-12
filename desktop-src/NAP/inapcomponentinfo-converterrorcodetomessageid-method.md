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
ms.openlocfilehash: 8c670585674713d114f6505a0c3211d599663545f6b06a40669f7fba8b7eddf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621728"
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



 

## <a name="remarks"></a>Remarques

Le **MessageID** retourné est utilisé par le système NAP pour récupérer une chaîne localisée.

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

 

 





