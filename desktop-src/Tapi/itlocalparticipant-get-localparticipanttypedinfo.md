---
description: La \_ méthode obtenir LocalParticipantTypedInfo obtient les informations sur les participants, telles que le nom du courrier électronique ou l’emplacement géographique.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'ITLocalParticipant :: get_LocalParticipantTypedInfo, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541639"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>ITLocalParticipant :: \_ LocalParticipantTypedInfo, méthode

La méthode **obtenir \_ LocalParticipantTypedInfo** obtient les informations sur les participants, telles que le nom du courrier électronique ou l’emplacement géographique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Infotype* \[ dans\]
</dt> <dd>

[**Participant \_ Identificateur \_ d’informations typées**](participant-typed-info.md) du type d’information requis.

</dd> <dt>

*ppInfo* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** qui contient les informations requises à la suite d’un retour réussi de la méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

L’application doit utiliser [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppInfo* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**\_infos de saisie du participant \_**](participant-typed-info.md)
</dt> </dl>

 

