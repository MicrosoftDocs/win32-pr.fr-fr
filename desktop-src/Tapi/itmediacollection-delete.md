---
description: La méthode Delete supprime le support correspondant à l’index spécifié.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: ITMediaCollection ::D méthode supprimable (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095745"
---
# <a name="itmediacollectiondelete-method"></a>ITMediaCollection ::D méthode supprimable

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **Delete** supprime le support correspondant à l’index spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* \[ dans\]
</dt> <dd>

Index du média à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                                                              | Description                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                                     | La méthode a réussi.<br/>                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                             | Le paramètre d' *index* a une valeur inférieure à 1 ou supérieure au nombre actuel d’éléments.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>                                            | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                                          |
| <dl> <dt>**E \_ échec**</dt> </dl>                                                   | Erreur interne (ne doit se produire que si un appel précédent a retourné une erreur).<br/>                      |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>                                                | Cette méthode n'est pas encore implémentée.<br/>                                                           |
| <dl> <dt>**HRESULT \_ à partir du \_ code d’erreur \_ (SDPBLB \_ conf \_ BLOB \_ détruit)**</dt> </dl> | L’objet BLOB SDP n’existe pas.<br/>                                                                   |



 

## <a name="remarks"></a>Notes

la plupart des listes C et C++ sont de base 0, mais cet index est basé sur 1 pour la compatibilité Visual Basic, ce qui signifie que le premier élément a un numéro d’index de 1.

## <a name="requirements"></a>Spécifications



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

 

 




