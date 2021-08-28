---
description: La méthode GetClassWindowStyles récupère les styles de classe et les styles de fenêtre de la fenêtre.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Méthode CBaseWindow. GetClassWindowStyles (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074627"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Méthode CBaseWindow. GetClassWindowStyles

La `GetClassWindowStyles` méthode récupère les styles de classe et les styles de fenêtre de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pClassStyles* 
</dt> <dd>

Pointeur vers une variable qui reçoit les styles de classe.

</dd> <dt>

*pWindowStyles* 
</dt> <dd>

Pointeur vers une variable qui reçoit les styles de fenêtre.

</dd> <dt>

*pWindowStylesEx* 
</dt> <dd>

Pointeur vers une variable qui reçoit les styles de fenêtre étendus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une chaîne de texte statique qui contient le nom de la classe.

## <a name="remarks"></a>Remarques

La méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) appelle cette méthode pour récupérer les styles de classe et les styles de fenêtre de la fenêtre.

Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter. L’exemple suivant illustre une implémentation possible :


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



L’objet utilise le style de classe pour le membre **lpszClassName** d’une structure WNDCLASS, qu’il transmet à la fonction **registerClass** . L’objet utilise les styles de fenêtre pour les paramètres *dwExStyle* et *dwStyle* de la fonction **CreateWindowEx** . Pour plus d’informations, consultez le kit de développement Platform SDK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




