---
description: 'IEnumMedia :: Skip, méthode-la méthode Skip ignore le nombre spécifié d’éléments dans la séquence d’énumération.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'IEnumMedia :: Skip, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084187"
---
# <a name="ienummediaskip-method"></a>IEnumMedia :: Skip, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **Skip** ignore le nombre spécifié d’éléments dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d'éléments à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                             | Description                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Le nombre d’éléments ignorés était *celt*.<br/>     |
| <dl> <dt>**S \_ false**</dt> </dl> | Le nombre d’éléments ignorés n’est pas *celt*.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




