---
description: La \_ méthode d’état d’extraction renvoie une variante \_ booléenne indiquant l’état du participant.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'ITParticipant :: get_Status, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1585c9605447e7b515885ecf9e30d060afb7a57d14c5b29a66025f2df9da05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060847"
---
# <a name="itparticipantget_status-method"></a>ITParticipant :: obtient l' \_ État, méthode

\[en **savoir \_ plus l’état** ne peut pas être utilisé dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode d' **\_ État d’extraction** renvoie une variante \_ booléenne indiquant l’état du participant.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pITStream* \[ dans\]
</dt> <dd>

Pointeur vers l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> <dt>

*pStatus* \[ à\]
</dt> <dd>

VARIANTE \_ true si le participant est activé sur le flux, variant \_ false s’il est désactivé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                              |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Méthode non implémentée.<br/>                                        |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>           |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pITStream* n’est pas un pointeur valide.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pITStream* ne pointe pas vers une interface valide.<br/> |



 

## <a name="remarks"></a>Remarques

L’activation ou la désactivation de l’état d’un participant sur un flux permet à une application de désactiver un participant donné.

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

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**Placer l' \_ État**](itparticipant-put-status.md)
</dt> </dl>

 

