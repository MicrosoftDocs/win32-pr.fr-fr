---
title: INapSoHConstructor Validate, méthode (NapProtocol. h)
description: Vérifie la validité du paquet SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Valider la méthode NAP
- Valider la méthode NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, Validate, méthode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413760"
---
# <a name="inapsohconstructorvalidate-method"></a>INapSoHConstructor :: Validate, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSoHConstructor :: Validate** vérifie la validité du paquet SOH.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*SOH* \[ dans\]
</dt> <dd>

Pointeur vers le paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) construit.

</dd> <dt>

*isRequest* \[ dans\]
</dt> <dd>

Valeur **booléenne** qui est **true** si le paquet est un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** s’il s’agit d’un **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                            | Description                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Le paquet SoH est valide.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Erreur d’autorisation, accès refusé.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite du système, impossible d’effectuer l’opération.<br/> |
| <dl> <dt>**\_paquet NAP E \_ non valide \_**</dt> </dl> | Le paquet SoH n’est pas valide.<br/>                              |



 

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





