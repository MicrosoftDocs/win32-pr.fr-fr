---
description: La méthode ReOrderCapabilities définit une nouvelle commande pour les fonctionnalités de format.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'ITFormatControl :: ReOrderCapabilities, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526543"
---
# <a name="itformatcontrolreordercapabilities-method"></a>ITFormatControl :: ReOrderCapabilities, méthode

\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **ReOrderCapabilities** définit une nouvelle commande pour les fonctionnalités de format.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwIndices* \[ dans\]
</dt> <dd>

Index du format en cours de réorganisation.

</dd> <dt>

*pfEnabled* \[ dans\]
</dt> <dd>

Indique si le format doit être activé ou désactivé.

</dd> <dt>

*pfPublicize* \[ dans\]
</dt> <dd>

Indique si le format doit être rendu disponible.

</dd> <dt>

*dwNumIndices* \[ dans\]
</dt> <dd>

Nouveau numéro d’index pour le format.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="remarks"></a>Notes

La méthode [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) doit être appelée avant d’utiliser cette méthode.

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
</dt> <dt>

[**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




