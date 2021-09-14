---
description: La méthode EnumerateStreams énumère les flux en cours avec les participants. Cette méthode est fournie pour les applications C et C++. les applications clientes Automation, telles que celles écrites en Visual Basic, doivent utiliser la \_ méthode Flux.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'ITParticipant :: EnumerateStreams, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193487"
---
# <a name="itparticipantenumeratestreams-method"></a>ITParticipant :: EnumerateStreams, méthode

\[**EnumerateStreams** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **EnumerateStreams** énumère les flux en cours avec les participants. Cette méthode est fournie pour les applications C et C++. les applications clientes Automation, telles que celles écrites en Visual Basic, doivent utiliser la méthode [**\_ Flux**](itparticipant-get-streams.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnumStream* \[ à\]
</dt> <dd>

Pointeur vers le pointeur d’interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                     | Signification                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le paramètre *ppEnumStream* n’est pas un pointeur valide.<br/> |



 

## <a name="remarks"></a>Notes

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) retournée par **ITParticipant :: EnumerateStreams**. L’application doit appeler **Release** sur l’interface **IEnumStream** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**recevoir \_ Flux**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




