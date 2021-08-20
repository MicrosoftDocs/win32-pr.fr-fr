---
title: Méthode INapComponentConfig IsUISupported (NapCommon. h)
description: Spécifie si le composant prend en charge une interface utilisateur personnalisée.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Méthode IsUISupported NAP
- Méthode IsUISupported NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e343b037e4f77b4c1e342ffa78278854b11d714e09e9e57188d83fc9f93a180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134487"
---
# <a name="inapcomponentconfigisuisupported-method"></a>INapComponentConfig :: IsUISupported, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **IsUISupported** spécifie si le composant prend en charge une interface utilisateur personnalisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsSupported* \[ à\]
</dt> <dd>

Pointeur vers un booléen dont la valeur est **true** si le composant prend en charge une interface utilisateur personnalisée et la valeur **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'opération a réussi.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

L’interface utilisateur personnalisée d’un composant doit être lancée à l’aide de [**INapComponentConfig :: InvokeUI**](inapcomponentconfig-invokeui.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





