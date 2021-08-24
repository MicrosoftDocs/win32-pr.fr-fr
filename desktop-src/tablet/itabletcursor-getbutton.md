---
description: Récupère l’objet bouton spécifié à partir d’un stylet de tablette.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'ITabletCursor :: GetButton, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938629"
---
# <a name="itabletcursorgetbutton-method"></a>ITabletCursor :: GetButton, méthode

Récupère l’objet bouton spécifié à partir d’un stylet de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iButton* \[ dans\]
</dt> <dd>

Identificateur du bouton à récupérer.

</dd> <dt>

*ppButton* \[ à\]
</dt> <dd>

Objet bouton spécifié par le paramètre *iButton* .

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

[**Interface ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




