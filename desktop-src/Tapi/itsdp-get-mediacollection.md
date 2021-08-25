---
description: La \_ méthode obtenir MediaCollection obtient un pointeur vers l’interface ITMediaCollection pour la Conférence.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'ITSdp :: get_MediaCollection, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf358089a394775c753adc0642897021e91df5bfcd5f23418e638df82db03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774509"
---
# <a name="itsdpget_mediacollection-method"></a>ITSdp :: \_ MediaCollection, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ MediaCollection** obtient un pointeur vers l’interface [**ITMediaCollection**](itmediacollection.md) pour la Conférence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMediaCollection* \[ à\]
</dt> <dd>

Pointeur vers [**ITMediaCollection**](itmediacollection.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                                                           | Signification                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                            | La méthode a réussi.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | Le paramètre *ppMediaCollection* n’est pas un pointeur valide.<br/>                        |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>                                   | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                             |
| <dl> <dt>**E \_ échec**</dt> </dl>                                          | Erreur non spécifiée.<br/>                                                               |
| <dl> <dt>**HRESULT \_ à partir du \_ code d’erreur \_ (erreur de \_ données non valides \_ )**</dt> </dl> | Une erreur interne s’est produite, généralement en raison de l’échec d’une méthode précédente.<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>                                       | Cette méthode n'est pas encore implémentée.<br/>                                              |



 

## <a name="remarks"></a>Remarques

Un pointeur [**ITMediaCollection**](itmediacollection.md) peut également être obtenu à l’aide de **QueryInterface**.

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITMediaCollection**](itmediacollection.md) retournée par **ITSdp :: \_ MediaCollection**. L’application doit appeler **Release** sur l’interface **ITMediaCollection** pour libérer les ressources qui lui sont associées.

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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




