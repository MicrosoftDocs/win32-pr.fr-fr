---
description: Retourne le nombre d’objets Cursor associés à la tablette.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'ITablet :: GetCursorCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524400"
---
# <a name="itabletgetcursorcount-method"></a>ITablet :: GetCursorCount, méthode

Retourne le nombre d’objets Cursor associés à la tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcCurs* \[ à\]
</dt> <dd>

Nombre d’objets Cursor associés à la tablette.

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

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




