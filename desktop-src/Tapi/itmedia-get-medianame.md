---
description: La \_ méthode obtenir MEDIANAME obtient le nom du support. Les médias définis sont audio, vidéo, tableau blanc, texte et données.
ms.assetid: 4afb24f9-582e-420d-8bda-772a3dc4d96c
title: 'ITMedia :: get_MediaName, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43cfa49af8b16138c2e92b2ea6296eb47f44b3d22b542d464e2bb87fc15b71e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060907"
---
# <a name="itmediaget_medianame-method"></a>ITMedia :: obtient la \_ méthode MEDIANAME

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ MEDIANAME** obtient le nom du support. Les médias définis sont audio, vidéo, tableau blanc, texte et données.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MediaName(
  [out] BSTR *ppMediaName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMediaName* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** contenant le nom du média, tel que l’audio.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppMediaName* n’est pas un pointeur valide.<br/>  |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppMediaName* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia ::p ut \_ MEDIANAME**](itmedia-put-medianame.md)
</dt> </dl>

 

