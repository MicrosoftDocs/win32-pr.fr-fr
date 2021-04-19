---
description: La \_ méthode obtenir ParticipantFromSubStream permet à une application de détecter les participants associés à un sous-flux donné.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'ITParticipantSubStreamControl :: get_ParticipantFromSubStream, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544028"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a>ITParticipantSubStreamControl :: \_ ParticipantFromSubStream, méthode

\[en **savoir \_ plus ParticipantFromSubStream** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ ParticipantFromSubStream** permet à une application de détecter les participants associés à un sous-flux donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pITSubStream* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> <dt>

*ppParticipant* \[ à\]
</dt> <dd>

Pointeur vers un tableau de pointeurs d’interface [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                     | Description                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | La méthode a réussi.<br/>                                                       |
| <dl> <dt>**\_pointeur E**</dt> </dl>       | Le paramètre *pITSubStream* ou *ppParticipant* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Le paramètre *pITSubStream* ne pointe pas vers une interface valide.<br/>         |
| <dl> <dt>**\_NOitems TAPI E \_**</dt> </dl> | Aucun participant n’est associé au sous-flux.<br/>                |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>   | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

