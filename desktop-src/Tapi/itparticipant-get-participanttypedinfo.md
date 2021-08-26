---
description: La \_ méthode obtenir ParticipantTypedInfo obtient une représentation BSTR du type d’informations nécessaires, par exemple PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'ITParticipant :: get_ParticipantTypedInfo, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43afb80b0f1161cf0060c8492576ade4f682af44cb4b2dbb13ab49d2c65aab66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867149"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>ITParticipant :: \_ ParticipantTypedInfo, méthode

\[en **savoir \_ plus ParticipantTypedInfo** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ ParticipantTypedInfo** obtient une représentation **BSTR** du type d’informations nécessaires, par exemple PTI \_ EMAILADDRESS.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Infotype* \[ dans\]
</dt> <dd>

[**Participant \_ \_**](participant-typed-info.md) Descripteur d’informations typées du type d’informations nécessaires.

</dd> <dt>

*ppInfo* \[ à\]
</dt> <dd>

Pointeur vers la représentation **BSTR** des informations nécessaires.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                    | Description                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>           | La méthode a réussi.<br/>                                    |
| <dl> <dt>**E \_ échec**</dt> </dl>         | échec de Stockage d’informations dans *ppInfo* .<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Le paramètre *infotype* n’est pas valide.<br/>               |
| <dl> <dt>**\_pointeur E**</dt> </dl>      | Le paramètre *ppInfo* n’est pas un pointeur valide.<br/>       |
| <dl> <dt>**initem de TAPI \_ E \_**</dt> </dl> | L’interface TAPI n’a pas d’informations sur le type spécifié.<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>  | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppInfo* .

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

[**\_infos de saisie du participant \_**](participant-typed-info.md)
</dt> <dt>

[**types de médias**](tapimediatype--constants.md)
</dt> </dl>

 

