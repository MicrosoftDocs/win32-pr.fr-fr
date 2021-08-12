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
ms.openlocfilehash: a55805d85cc6a809a915f3998ab1b3dd218bd35a10b3b0044ff7c78130a72d97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621170"
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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





