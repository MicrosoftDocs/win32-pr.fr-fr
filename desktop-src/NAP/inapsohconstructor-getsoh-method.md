---
title: Méthode INapSoHConstructor GetSoH (NapProtocol. h)
description: Récupère le paquet SoHRequest ou SoHResponse construit.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Méthode GetSoH NAP
- Méthode GetSoH NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, méthode GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103537"
---
# <a name="inapsohconstructorgetsoh-method"></a>INapSoHConstructor :: GetSoH, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHConstructor :: GetSoH** récupère le paquet SoHRequest ou SoHResponse construit.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SOH* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers le paquet [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ou **SoHResponse** construit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                     | Description                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L’opération a réussi.<br/>                                   |
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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





