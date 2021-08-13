---
description: La \_ méthode obtenir SessionVersion obtient 32 la valeur de protocole NTP (Network Time Protocol, ou NTP) qui sert de version de session.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'ITSdp :: get_SessionVersion, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7661fb5f133d214748991510d56387991872fa69243353b5144623a1ef19f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476589"
---
# <a name="itsdpget_sessionversion-method"></a>ITSdp :: \_ SessionVersion, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

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



 

## <a name="remarks"></a>Remarques

la valeur de retour de cette méthode peut être **ULONG**, mais Visual Basic ne prend pas en charge le type **ulong** . Un **double** est le plus petit type suivant qui englobe la plage entière de valeurs requises.

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

 

 




