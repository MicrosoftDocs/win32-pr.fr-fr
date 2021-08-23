---
description: La \_ méthode obtenir des participants crée une collection de participants associés à la Conférence en cours.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'ITParticipantControl :: get_Participants, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d61d12de18e30bd86d42fd1aa75aed2048c42e487e019eabe3da6d65e70a9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864710"
---
# <a name="itparticipantcontrolget_participants-method"></a>ITParticipantControl :: obtient la \_ méthode des participants

\[en **savoir \_ plus les Participants** ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir des \_ participants** crée une collection de participants associés à la Conférence en cours. Cette méthode est fournie pour les applications clientes Automation, telles que celles écrites en Visual Basic. Les applications C et C++ doivent utiliser la méthode [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVariant* \[ à\]
</dt> <dd>

Pointeur vers un **Variant** contenant un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de pointeurs d’interface [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pVariant* n’est pas un pointeur valide.<br/>     |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITParticipant**](itparticipant.md) retournée par **ITParticipantControl :: obtient \_ participants**. L’application doit appeler **Release** sur l’interface **ITParticipant** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




