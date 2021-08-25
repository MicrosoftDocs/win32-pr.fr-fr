---
description: Se produit lorsque le curseur se déplace sur le digitaliseur de tablette.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'ITabletEventSink :: CursorMove, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 030fa5ba4adc725288d5135ccd24409d4fc02cddbc16da52aa375a275a73be5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843489"
---
# <a name="itableteventsinkcursormove-method"></a>ITabletEventSink :: CursorMove, méthode

Se produit lorsque le curseur se déplace sur le digitaliseur de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*tcid* 
</dt> <dd>

Dentifier unique du digitaliseur de tablette.

</dd> <dt>

*confirmation* 
</dt> <dd>

Identificateur unique du stylet de tablette.

</dd> <dt>

*hWnd* 
</dt> <dd>

Fenêtre sur laquelle le curseur a été déplacé.

</dd> <dt>

*xPos* 
</dt> <dd>

Position X du stylet.

</dd> <dt>

*PosY* 
</dt> <dd>

Position Y du stylet.

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

 

 




