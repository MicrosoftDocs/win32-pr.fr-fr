---
title: Méthode INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Récupère le nombre total d’attributs dans la SoH.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Méthode GetNumberOfAttributes NAP
- Méthode GetNumberOfAttributes NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, méthode GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508570"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a>INapSoHProcessor :: GetNumberOfAttributes, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHProcessor :: GetNumberOfAttributes** récupère le nombre total d’attributs dans la SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*attributeCount* \[ à\]
</dt> <dd>

Pointeur vers le nombre d’attributs retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Opération réussie.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite du système, impossible d’effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





