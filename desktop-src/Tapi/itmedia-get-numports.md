---
description: La \_ méthode obtenir NumPorts obtient le nombre de ports nécessaires pour la session. La session utilise le nombre spécifié de ports à partir de la valeur retournée par \_ StartPort.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'ITMedia :: get_NumPorts, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 928f1622c26159720a5eaabe42a16dd5513705c4d9abe9ad75db47160ab3e218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865002"
---
# <a name="itmediaget_numports-method"></a>ITMedia :: \_ NumPorts, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ NumPorts** obtient le nombre de ports nécessaires pour la session. La session utilise le nombre spécifié de ports à partir de la valeur retournée par [**\_ StartPort**](itmedia-get-startport.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNumPorts* \[ à\]
</dt> <dd>

Pointeur vers le nombre de ports.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pNumPorts* n’est pas un pointeur valide.<br/>    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> </dl>

 

 




