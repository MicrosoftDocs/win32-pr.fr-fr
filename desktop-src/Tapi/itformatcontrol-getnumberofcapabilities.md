---
description: La méthode GetNumberOfCapabilities récupère le nombre de fonctionnalités associées au format actuel.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'ITFormatControl :: GetNumberOfCapabilities, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533350"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a>ITFormatControl :: GetNumberOfCapabilities, méthode

\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetNumberOfCapabilities** récupère le nombre de fonctionnalités associées au format actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwCount* \[ à\]
</dt> <dd>

Nombre de fonctionnalités.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




