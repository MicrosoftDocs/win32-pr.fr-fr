---
description: La \_ méthode put LocalParticipantTypedInfo définit les informations sur les participants.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: ITLocalParticipant ::p ut_LocalParticipantTypedInfo, méthode (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acca83d7ad68ed0974aaa2e7d4fb4755c11939d0711473c406cb09d78451ac41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774899"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>ITLocalParticipant ::p ut \_ LocalParticipantTypedInfo, méthode

La méthode **put \_ LocalParticipantTypedInfo** définit les informations sur les participants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Infotype* \[ dans\]
</dt> <dd>

[**Participant \_ Identificateur \_ d’informations typées**](participant-typed-info.md) du type d’information requis.

</dd> <dt>

*ppInfo* \[ dans\]
</dt> <dd>

**BSTR** contenant la nouvelle valeur requise pour les informations.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

L’application doit utiliser [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PpInfo* et utiliser [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.

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

 

