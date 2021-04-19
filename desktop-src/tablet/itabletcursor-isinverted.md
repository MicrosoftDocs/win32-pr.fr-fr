---
description: Indique si le stylet est à l’envers.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'ITabletCursor :: IsInverted, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524327"
---
# <a name="itabletcursorisinverted-method"></a>ITabletCursor :: IsInverted, méthode

Indique si le stylet est à l’envers.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                             | Description                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Le stylet est inversé.<br/>        |
| <dl> <dt>**S \_ false**</dt> </dl> | Le stylet n’est pas inversé.<br/>    |
| <dl> <dt>**E \_ échec**</dt> </dl>  | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITabletCursor**](itabletcursor.md)
</dt> <dt>

[**Interface ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

 




