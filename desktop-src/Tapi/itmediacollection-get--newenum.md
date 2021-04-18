---
description: La \_ \_ méthode obtenir NewEnum retourne un énumérateur pour la collection.
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'ITMediaCollection :: get__NewEnum, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfa5655d70026fe2c481aedad0e76923f4caa646
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533361"
---
# <a name="itmediacollectionget__newenum-method"></a>ITMediaCollection :: obtient la \_ \_ méthode NewEnum

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ \_ NewEnum** retourne un énumérateur pour la collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ à\]
</dt> <dd>

Pointeur vers une interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur un objet énumérateur pour la collection.

Appelez la méthode [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’interface **IUnknown** retournée pour obtenir un pointeur vers une interface d’énumération [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur la collection. **IEnumVARIANT** fournit un certain nombre de méthodes que vous pouvez utiliser pour itérer au sein de la collection.

Pour plus d'informations, consultez la section Notes qui suit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pval* n’est pas un pointeur valide.<br/>         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

Cette méthode est interchangeable avec la méthode [**\_ EnumerationIf**](itmediacollection-get-enumerationif.md) , sauf qu’elle retourne **IUnknown** au lieu de [**IEnumMedia**](ienummedia.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

