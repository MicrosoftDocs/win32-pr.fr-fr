---
description: La méthode d’extraction d' \_ URL obtient l’URL.
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'ITSdp :: get_Url, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a207c158d405ac0931e42aa19995d1d4b3078fd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542810"
---
# <a name="itsdpget_url-method"></a>ITSdp :: obtient l' \_ URL, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode d' **extraction d' \_ URL** obtient l’URL.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppUrl* \[ à\]
</dt> <dd>

Pointeur vers une représentation **BSTR** de l’URL.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppUrl* n’est pas un pointeur valide.<br/>        |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppUrl* .

Une URL est généralement utilisée pour référencer une page Web contenant des ressources supplémentaires ou des informations générales sur une conférence.

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

[**ITSdp : URL de :p ut \_**](itsdp-put-url.md)
</dt> </dl>

 

