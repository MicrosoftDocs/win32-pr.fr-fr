---
title: Méthode INapSoHConstructor AppendAttribute (NapProtocol. h)
description: Ajoute un TLV à la fin de la mémoire tampon SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Méthode AppendAttribute NAP
- Méthode AppendAttribute NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, méthode AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7d7ca4636d0eaeea35054dc5330b17f1360dffec5231922ad0acc357231c3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939586"
---
# <a name="inapsohconstructorappendattribute-method"></a>INapSoHConstructor :: AppendAttribute, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHConstructor :: AppendAttribute** ajoute un TLV à la fin de la mémoire tampon SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Énumération [**SoHAttributeType**](sohattributetype-enum.md) qui indique le type d’attribut du nouvel TLV.

</dd> <dt>

*valeur* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**SoHAttributeValue**](sohattributevalue-union.md) qui contient la valeur de la nouvelle TLV.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

Le [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV ne doit pas être ajouté à l’aide de cette fonction. Il est ajouté comme premier TLV par [**INapSoHConstructor :: Initialize**](inapsohconstructor-initialize-method.md) aux paquets SOH nouvellement construits.

Lors de l’ajout d’un attribut qui sera consommé par le système NAP, il ne doit pas être chiffré ou modifié de quelque manière que ce soit. Si le HealthEntity requiert le chiffrement/la vérification de l’intégrité (Mac) des informations privées, il doit être inclus uniquement dans l’attribut [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





