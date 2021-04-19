---
description: Récupère le nombre de boutons sur le stylet de tablette.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'ITabletCursor :: GetButtonCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521176"
---
# <a name="itabletcursorgetbuttoncount-method"></a>ITabletCursor :: GetButtonCount, méthode

Récupère le nombre de boutons sur le stylet de tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcButtons* \[ à\]
</dt> <dd>

Nombre de boutons sur le stylet de tablette.

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

[**Interface ITabletCursor**](itabletcursor.md)
</dt> </dl>

 

 




