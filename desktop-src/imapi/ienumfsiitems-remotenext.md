---
title: Méthode IEnumFsiItems RemoteNext
description: Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération. | Méthode IEnumFsiItems RemoteNext
ms.assetid: a5ae59ed-08d7-4225-9aec-91049789e8fe
keywords:
- Méthode RemoteNext IMAPi
- Méthode RemoteNext IMAPi, interface IEnumFsiItems
- Interface IEnumFsiItems IMAPi, méthode RemoteNext
topic_type:
- apiref
api_name:
- IEnumFsiItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b63c2d0a5223dd2ae282804b2a6dc5e2872a5c108ed885bdca5a0db862a4b75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062540"
---
# <a name="ienumfsiitemsremotenext-method"></a>IEnumFsiItems :: RemoteNext, méthode

Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoteNext(
  [in]  ULONG    celt,
  [out] IFsiItem **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d’éléments à récupérer.

</dd> <dt>

*rgelt* \[ à\]
</dt> <dd>

Tableau d’interfaces [**IFsiItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem) . Lorsque vous avez terminé, vous devez libérer chaque interface dans rgelt.

</dd> <dt>

*pceltFetched* \[ à\]
</dt> <dd>

Nombre d’éléments retournés dans rgelt. Vous pouvez affecter à *pceltFetched* la **valeur null** si *celt* est un. Sinon, initialisez la valeur de *pceltFetched* à 0 avant d’appeler cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

\_Un OK est retourné lorsque le nombre d’éléments demandés (*celt*) est retourné avec succès ou que le nombre d’éléments retournés (*pceltFetched*) est inférieur au nombre d’éléments demandés.

D’autres codes de réussite peuvent être retournés à la suite de l’implémentation. Les codes d’erreur suivants sont généralement renvoyés en cas d’échec de l’opération, mais ne représentent pas les seules valeurs d’erreur possibles :



| Code de retour                                                                                   | Description                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le pointeur n’est pas valide.<br/> Valeur : 0x80004003<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Impossible d’allouer la mémoire requise.<br/> Valeur : 0x8007000E<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un ou plusieurs arguments ne sont pas valides.<br/> Valeur : 0x80070057<br/>    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| MIDL<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumFsiItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems)
</dt> <dt>

[IEnumFsiItems :: suivant](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumfsiitems-next)
</dt> </dl>

 

 





