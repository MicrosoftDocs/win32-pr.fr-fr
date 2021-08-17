---
title: Méthode IEnumProgressItems RemoteNext
description: Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération. | Méthode IEnumProgressItems RemoteNext
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Méthode RemoteNext IMAPi
- Méthode RemoteNext IMAPi, interface IEnumProgressItems
- Interface IEnumProgressItems IMAPi, méthode RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daa2b33fdc356782837aadfe37186bc4cc2b493208fdc78ba645ada9e746582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884849"
---
# <a name="ienumprogressitemsremotenext-method"></a>IEnumProgressItems :: RemoteNext, méthode

Prend en charge un client distant qui souhaite récupérer un nombre spécifié d’éléments dans la séquence d’énumération

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
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

Tableau d’interfaces [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) . Lorsque vous avez terminé, vous devez libérer chaque interface dans rgelt.

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
| <dl> <dt>**E \_ Inattendue**</dt> </dl> | Une défaillance inattendue s'est produite.<br/> Valeur : 0x8000FFFF<br/>         |



 

## <a name="remarks"></a>Remarques

Si le nombre d’éléments restants dans la séquence est inférieur au nombre demandé, il récupère les éléments restants.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| MIDL<br/>                      | <dl> <dt>Imapi2fs. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumProgressItems**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[IEnumProgressItems :: suivant](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





