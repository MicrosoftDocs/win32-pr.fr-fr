---
description: La \_ méthode obtenir SessionVersion obtient 32 la valeur de protocole NTP (Network Time Protocol, ou NTP) qui sert de version de session.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'ITSdp :: get_SessionVersion, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541556"
---
# <a name="itsdpget_sessionversion-method"></a>ITSdp :: \_ SessionVersion, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ SessionVersion** obtient 32 la valeur de protocole NTP (Network Time Protocol, ou NTP) qui sert de version de session. Bien qu’elle soit générée automatiquement lors de la création de la session, l’utilisateur est responsable de sa modification lors de la modification du SDP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSessionVersion* \[ à\]
</dt> <dd>

Pointeur vers l’identificateur de version de session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pSessionVersion* n’est pas valide.<br/>           |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pSessionVersion* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>    |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                      |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                     |



 

## <a name="remarks"></a>Notes

La valeur de retour de cette méthode peut être **ULong**, mais Visual Basic ne prend pas en charge le type **ULong** . Un **double** est le plus petit type suivant qui englobe la plage entière de valeurs requises.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp ::p ut \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




