---
description: la \_ méthode obtenir Flux crée une collection de flux associés au participant actuel.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'ITParticipant :: get_Streams, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b66447cd320110db45e1624d677c9b76e518f926da341805bd7de992d0e0eec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003287"
---
# <a name="itparticipantget_streams-method"></a>ITParticipant :: obtient \_ Flux méthode

\[**le \_ Flux de récupération** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

la méthode **obtenir \_ Flux** crée une collection de flux associés au participant actuel. Cette méthode est fournie pour les applications clientes Automation, telles que celles écrites en Visual Basic. Les applications C et C++ doivent utiliser la méthode [**EnumerateStreams**](itparticipant-enumeratestreams.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVariant* \[ à\]
</dt> <dd>

Pointeur vers un **Variant** contenant un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de pointeurs d’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pVariant* n’est pas un pointeur valide.<br/>     |



 

## <a name="remarks"></a>Remarques

l’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) retournée par **ITParticipant :: obtient \_ Flux**. L’application doit appeler **Release** sur l’interface **ITStream** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Configuration requise



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

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

