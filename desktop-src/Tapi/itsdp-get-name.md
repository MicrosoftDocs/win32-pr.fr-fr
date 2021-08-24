---
description: La \_ méthode obtenir le nom obtient le nom de la session.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'ITSdp :: get_Name, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 930aaa1edcfb93f6a02a4ebe97acbbfcc1cfd42e8187d0ea14cf661c7ad7f66c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012889"
---
# <a name="itsdpget_name-method"></a>ITSdp :: méthode d’extraction de \_ nom

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir le \_ nom** obtient le nom de la session. Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII. (Dans le cas contraire, il peut s’agir d’une chaîne **BSTR** .)

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppName* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** contenant le nom de session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppName* n’est pas un pointeur valide.<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppName* .

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

[**ITSdp ::p nom de l’UT \_**](itsdp-put-name.md)
</dt> </dl>

 

