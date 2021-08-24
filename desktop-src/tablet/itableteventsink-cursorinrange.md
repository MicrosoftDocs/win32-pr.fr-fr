---
description: Se produit lorsqu’un stylet est dans la plage de détection du digitaliseur.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'ITabletEventSink :: CursorInRange, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2c9878b4c3cd28727c5d54e59a52f3fe85a44832203f70b6ff042c6beeb579dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883479"
---
# <a name="itableteventsinkcursorinrange-method"></a>ITabletEventSink :: CursorInRange, méthode

Se produit lorsqu’un stylet est dans la plage de détection du digitaliseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TCID* \[ dans\]
</dt> <dd>

Identificateur de l’objet tablette ayant détecté le stylet.

</dd> <dt>

*confirmation* 
</dt> <dd>

Identificateur de l’objet stylet qui est compris dans la plage du digitaliseur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




