---
description: La méthode SwitchTerminalToSubStream définit un terminal sur le sous-flux du participant.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'ITParticipantSubStreamControl :: SwitchTerminalToSubStream, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f211d4f3ff0f01801fb5497d36d81fa46e43397d8b69227180b022c9e74a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774649"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>ITParticipantSubStreamControl :: SwitchTerminalToSubStream, méthode

\[**SwitchTerminalToSubStream** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SwitchTerminalToSubStream** définit un terminal sur le sous-flux du participant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pITTerminal* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

</dd> <dt>

*pITSubStream* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                     | Description                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | La méthode a réussi.<br/>                                                                       |
| <dl> <dt>**E \_ inattendu**</dt> </dl>    | Impossible d’accéder aux informations sur le participant pour le flux.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Le paramètre *pParticipant* ou *pITSubStream* ne pointe pas vers une interface valide.<br/> |
| <dl> <dt>**\_NOitems TAPI E \_**</dt> </dl> | Le sous-flux n’est pas prêt.<br/>                                                             |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>   | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                                    |



 

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
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

