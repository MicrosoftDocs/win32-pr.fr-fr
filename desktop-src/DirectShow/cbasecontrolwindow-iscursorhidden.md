---
description: La méthode IsCursorHidden récupère l’état actuel du \_ membre de données m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Méthode CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f7e64b056715a9f67255b6c16f62c64b65361562489ef47a37dd63548dd6e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793739"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a>Méthode CBaseControlWindow. IsCursorHidden

La `IsCursorHidden` méthode récupère l’état actuel du membre de données **m \_ bCursorHidden** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CursorHidden* 
</dt> <dd>

Pointeur vers la valeur de **m \_ bCursorHidden**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas d’appel sans paramètre, retourne OATRUE si le curseur est masqué ou OAFALSE si le curseur est visible.

## <a name="remarks"></a>Remarques

Les objets internes doivent appeler cette fonction membre sans le paramètre *CursorHidden* pour éviter de verrouiller la section critique. Les objets externes accèdent à cette fonction membre avec le paramètre *CursorHidden* via la méthode [**IVideoWindow :: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




