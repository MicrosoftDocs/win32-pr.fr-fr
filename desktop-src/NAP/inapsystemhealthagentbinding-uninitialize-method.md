---
title: INapSystemHealthAgentBinding méthode Uninitialize (NapSystemHealthAgent. h)
description: Fait en sorte que le NapAgent libère toutes ses références aux pointeurs COM de l’agent d’intégrité système.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Uninitialize la méthode NAP
- Uninitialize Method NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, Uninitialize, méthode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011656"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>INapSystemHealthAgentBinding :: Uninitialize, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **INapSystemHealthAgentBinding :: Uninitialize** force NapAgent à libérer toutes ses références aux pointeurs com de l’agent d’intégrité système.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Uninitialize();
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

NapAgent bloque l’exécution de cet appel de méthode jusqu’à ce que tous les appels existants sur les interfaces de liaison et de rappel se terminent.

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

 

 





