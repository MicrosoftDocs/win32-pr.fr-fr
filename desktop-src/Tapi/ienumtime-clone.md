---
description: La méthode Clone crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'IEnumTime :: Clone, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543913"
---
# <a name="ienumtimeclone-method"></a>IEnumTime :: Clone, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **clone** crée un autre énumérateur qui contient le même état d’énumération que l’énumérateur actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnum* \[ à\]
</dt> <dd>

Pointeur vers le nouvel objet [**IEnumTime**](ienumtime.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppEnum* n’est pas un pointeur valide.<br/>       |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>  | A échoué pour des raisons inconnues.<br/>                          |



 

## <a name="remarks"></a>Notes

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumTime**](ienumtime.md) retournée par **IEnumTime :: Clone**. L’application doit appeler **Release** sur l’interface **IEnumTime** pour libérer les ressources qui lui sont associées.

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

 

 




