---
description: La \_ méthode obtenir SubStreamFromParticipant permet à une application de détecter les sous-flux associés à un participant donné.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'ITParticipantSubStreamControl :: get_SubStreamFromParticipant, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526697"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>ITParticipantSubStreamControl :: \_ SubStreamFromParticipant, méthode

\[en **savoir \_ plus SubStreamFromParticipant** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ SubStreamFromParticipant** permet à une application de détecter les sous-flux associés à un participant donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pParticipant* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**ITParticipant**](itparticipant.md) .

</dd> <dt>

*ppITSubStream* \[ à\]
</dt> <dd>

Pointeur vers un tableau de pointeurs d’interface [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                                 |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppITSubStream* n’est pas un pointeur valide.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pParticipant* ne pointe pas vers une interface valide.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>  | Impossible d’accéder aux informations sur le participant du flux.<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>              |



 

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

 

