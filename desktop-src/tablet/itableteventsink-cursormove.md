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
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541984"
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
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




