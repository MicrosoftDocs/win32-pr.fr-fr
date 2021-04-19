---
description: Le sous-flux d’extraction \_ obtient un pointeur vers un tableau d’interfaces ITSubStream représentant les sous-flux impliqués dans l’événement.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'ITParticipantEvent :: get_SubStream, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542607"
---
# <a name="itparticipanteventget_substream-method"></a>ITParticipantEvent :: obtient la méthode de sous- \_ flux

\[en **savoir \_ plus** Le sous-flux ne peut pas être utilisé dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le sous- **\_ flux d’extraction** obtient un pointeur vers un tableau d’interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) représentant les sous-flux impliqués dans l’événement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSubStream* \[ à\]
</dt> <dd>

Pointeur vers un tableau de pointeurs [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                           | Signification                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_NOitems TAPI E \_**</dt> </dl> | Aucun sous-flux n’est associé à l’événement.<br/>   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>   | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>       | Le paramètre *ppSubStream* n’est pas un pointeur valide.<br/>  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

