---
description: La méthode GetEmailNames obtient un tableau de noms de messagerie associés à l’objet blob de conférence.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'ITSdp :: GetEmailNames, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74ea369210a6ca32e47bb3359000195c544374b7352da96570f6d0f58f2af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140262"
---
# <a name="itsdpgetemailnames-method"></a>ITSdp :: GetEmailNames, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetEmailNames** obtient un tableau de noms de messagerie associés à l’objet blob de conférence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAddresses* \[ à\]
</dt> <dd>

Pointeur **Variant** vers un SafeArray de **BSTR** répertoriant les adresses de messagerie.

</dd> <dt>

*pNames* \[ à\]
</dt> <dd>

Pointeur de **type Variant** vers un SafeArray de noms de liste de **BSTR**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                              |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pAddresses* ou *pNames* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>           |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                             |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                            |



 

## <a name="remarks"></a>Remarques

Les listes que *pAddresses* et *pNames* pointent sont de la même longueur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




