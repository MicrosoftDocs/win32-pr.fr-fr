---
description: La méthode Create crée un nouveau média avec les propriétés par défaut, l’ajoute à la collection à l’index spécifié et retourne un pointeur vers l’interface ITMedia.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'ITMediaCollection :: Create, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095749"
---
# <a name="itmediacollectioncreate-method"></a>ITMediaCollection :: Create, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **Create** crée un nouveau média avec les propriétés par défaut, l’ajoute à la collection à l’index spécifié et retourne un pointeur vers l’interface [**ITMedia**](itmedia.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Index du nouvel élément. La valeur minimale pour l’index est 1, et la valeur maximale pour l’index est le nombre actuel d’éléments + 1.

</dd> <dt>

*ppMedia* \[ à\]
</dt> <dd>

Pointeur vers l’interface [**ITMedia**](itmedia.md) créée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppMedia* n’est pas un pointeur valide.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre d' *index* n’est pas valide.<br/>                  |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

la plupart des listes C et C++ sont de base 0, mais cet index est basé sur 1 pour la compatibilité Visual Basic, ce qui signifie que le premier élément a un numéro d’index de 1.

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITMedia**](itmedia.md) retournée par **ITMediaCollection :: Create**. L’application doit appeler **Release** sur l’interface [**ITMedia**](itmedia.md) pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Spécifications



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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




