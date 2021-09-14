---
title: INapSoHProcessor GetAttribute, méthode (NapProtocol. h)
description: Récupère le type et la valeur d’attribut, en fonction de l’emplacement de l’attribut.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Méthode GetAttribute NAP
- GetAttribute, méthode NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, GetAttribute, méthode
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011671"
---
# <a name="inapsohprocessorgetattribute-method"></a>INapSoHProcessor :: GetAttribute, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHProcessor :: GetAttribute** récupère le type et la valeur de l’attribut, en fonction de l’emplacement de l’attribut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributeLocation* \[ dans\]
</dt> <dd>

Emplacement (index) de l’attribut dont le type et la valeur doivent être récupérés. La valeur de *attributeLocation* est retournée à partir d’un appel antérieur à [**INapSoHProcessor :: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*type* \[ à\]
</dt> <dd>

Pointeur vers une structure [**SoHAttributeType**](sohattributetype-enum.md) qui spécifie le type de l’attribut dans *valeur*.

</dd> <dt>

*valeur* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers une structure [**SoHAttributeValue**](sohattributevalue-union.md) qui contient la valeur de l’attribut, telle que définie par le *type*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

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

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





