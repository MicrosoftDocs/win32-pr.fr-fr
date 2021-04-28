---
description: 'IEnumTime :: Next, méthode-la méthode suivante obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'IEnumTime :: Next, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118387"
---
# <a name="ienumtimenext-method"></a>IEnumTime :: Next, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **suivante** obtient le nombre spécifié d’éléments suivant dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d’éléments demandés.

</dd> <dt>

*pval* \[ à\]
</dt> <dd>

Pointeur vers l’interface [**ITTime**](ittime.md) .

</dd> <dt>

*pceltFetched* \[ à\]
</dt> <dd>

Pointeur vers le nombre d’éléments réellement fournis. Peut avoir la **valeur null** si *celt* a la valeur 1.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                     | Signification                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | La méthode a retourné la valeur *celt* Number of Elements.<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | Le nombre d’éléments restants était inférieur à *celt*.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Le paramètre *pval* n’est pas un pointeur valide.<br/>       |



 

## <a name="remarks"></a>Notes 

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITTime**](ittime.md) retournée par **IEnumTime :: Next**. L’application doit appeler **Release** sur l’interface **ITTime** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




