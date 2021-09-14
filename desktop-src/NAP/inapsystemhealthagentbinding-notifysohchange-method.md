---
title: Méthode INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: Est utilisé par les Sha lorsque leur SoH change.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Méthode NotifySoHChange NAP
- Méthode NotifySoHChange NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, méthode NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011657"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>INapSystemHealthAgentBinding :: NotifySoHChange, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentBinding :: NotifySoHChange** est utilisée par les Sha lorsque leur SOH change.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

D’autres codes d’erreur spécifiques à COM peuvent également être retournés.



| Code de retour                                                                                             | Description                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Opération réussie.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erreur d’autorisation, accès refusé.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite du système, impossible d’effectuer l’opération.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ non \_ initialisé**</dt> </dl> | L’algorithme SHA n’a pas été précédemment initialisé.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ déconnecté**</dt> </dl>     | Le NapAgent a été arrêté. Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.<br/> |



 

## <a name="remarks"></a>Notes

SHA ne doit pas appeler cette API de façon spéculative, car cela entraîne un échange SoH sur le câble. Les appels à cette API doivent être effectués uniquement lorsque cela est nécessaire.

NapAgent ne contient pas ce thread pour traiter la modification de SoH. Au lieu de cela, il retourne immédiatement et traite la modification de manière asynchrone.

L’algorithme SHA doit appeler [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





