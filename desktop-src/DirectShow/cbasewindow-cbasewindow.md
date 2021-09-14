---
description: Méthode constructeur CBaseWindow. CBaseWindow.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Constructeur CBaseWindow. CBaseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923779"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Constructeur CBaseWindow. CBaseWindow

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bDoGetDC* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut récupérer le contexte de périphérique (Device Context).

</dd> <dt>

*bPostToDestroy* 
</dt> <dd>

Valeur booléenne qui spécifie la variable membre [**CBaseWindow :: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Après avoir créé l’objet, appelez la méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) pour créer la fenêtre. **PrepareWindow** est une méthode virtuelle. Elle appelle [**CBaseWindow :: InitialiseWindow**](cbasewindow-initialisewindow.md), également une méthode virtuelle. Ces méthodes sont séparées du constructeur afin que les classes dérivées puissent les remplacer, si nécessaire.

Si la valeur du paramètre *bDoGetDC* est **true**, l' `CBaseWindow` objet récupère un handle vers le contexte de périphérique (DC) de la fenêtre et le stocke dans la variable membre [**CBaseWindow :: m \_ HDC**](cbasewindow-m-hdc.md) . L’objet crée également un contrôleur de stockage de mémoire compatible, qu’il stocke dans la variable membre [**CBaseWindow :: m \_ MemoryDC**](cbasewindow-m-memorydc.md) . Ces actions se produisent dans la méthode **InitialiseWindow** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




