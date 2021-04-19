---
description: La méthode d’extraction \_ EnumerationIf retourne l’interface d’énumération IEnumTime qui énumère ITTime.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'ITTimeCollection :: get_EnumerationIf, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525425"
---
# <a name="ittimecollectionget_enumerationif-method"></a>ITTimeCollection :: \_ EnumerationIf, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode d' **extraction \_ EnumerationIf** retourne l’interface d’énumération [**IEnumTime**](ienumtime.md) qui énumère [**ITTime**](ittime.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pval* \[ à\]
</dt> <dd>

Pointeur vers l’interface [**IEnumTime**](ienumtime.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pval* n’est pas un pointeur valide.<br/>         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

Cette méthode est interchangeable avec l’opération d’extraction de la valeur [**\_ \_ NewEnum**](ittimecollection-get--newenum.md) , sauf qu’elle retourne [**IEnumTime**](ienumtime.md) au lieu de **IUnknown**.

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumTime**](ienumtime.md) retournée par **ITTimeCollection :: \_ EnumerationIf**. L’application doit appeler **Release** sur l’interface [**IEnumTime**](ienumtime.md) pour libérer les ressources qui lui sont associées.

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
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




