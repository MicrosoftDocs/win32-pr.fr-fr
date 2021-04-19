---
description: La \_ méthode obtenir MediaTypes obtient les types de média associés à un participant.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'ITParticipant :: get_MediaTypes, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540138"
---
# <a name="itparticipantget_mediatypes-method"></a>ITParticipant :: \_ MediaTypes, méthode

\[en **savoir \_ plus MediaTypes** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ MediaTypes** obtient les [**types de média**](tapimediatype--constants.md) associés à un participant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*plMediaType* \[ à\]
</dt> <dd>

Pointeur vers les indicateurs de type de média, tels que la \_ vidéo TAPIMEDIATYPE.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *plMediaType* n’est pas un pointeur valide.<br/>  |



 

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

[**types de médias**](tapimediatype--constants.md)
</dt> </dl>

 

 




