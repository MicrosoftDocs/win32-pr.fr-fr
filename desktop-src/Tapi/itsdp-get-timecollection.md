---
description: La \_ méthode obtenir TimeCollection obtient un pointeur vers une interface ITTimeCollection pour la Conférence.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'ITSdp :: get_TimeCollection, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d52760de1cac36206269d9e3d890bb9383ce331a11d061c74a8c047ee01010b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060837"
---
# <a name="itsdpget_timecollection-method"></a>ITSdp :: \_ TimeCollection, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ TimeCollection** obtient un pointeur vers une interface [**ITTimeCollection**](ittimecollection.md) pour la Conférence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppTimeCollection* \[ à\]
</dt> <dd>

Pointeur vers [**ITTimeCollection**](ittimecollection.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                                                           | Signification                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                            | La méthode a réussi.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | Le paramètre *ppTimeCollection* n’est pas un pointeur valide.<br/>                         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>                                   | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                             |
| <dl> <dt>**E \_ échec**</dt> </dl>                                          | Erreur non spécifiée.<br/>                                                               |
| <dl> <dt>**HRESULT \_ à partir du \_ code d’erreur \_ (erreur de \_ données non valides \_ )**</dt> </dl> | Une erreur interne s’est produite, généralement en raison de l’échec d’une méthode précédente.<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>                                       | Cette méthode n'est pas encore implémentée.<br/>                                              |



 

## <a name="remarks"></a>Remarques

Un pointeur [**ITTimeCollection**](ittimecollection.md) peut également être obtenu à l’aide de **QueryInterface**.

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITTimeCollection**](ittimecollection.md) retournée par **ITSdp :: \_ TimeCollection**. L’application doit appeler **Release** sur l’interface **ITTimeCollection** pour libérer les ressources qui lui sont associées.

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
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> </dl>

 

 




