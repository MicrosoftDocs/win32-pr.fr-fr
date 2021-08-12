---
description: La \_ méthode obtenir le propriétaire récupère le propriétaire de la fenêtre active.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Méthode CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a64325fddebc410c5a75a5c2fb8811241012feb6a046b9059897f9b13e0206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660512"
---
# <a name="cbasecontrolwindowget_owner-method"></a>CBaseControlWindow. obten, \_ méthode de propriétaire

La `get_Owner` méthode récupère le propriétaire de la fenêtre active.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Propriétaire* 
</dt> <dd>

Pointeur vers le propriétaire de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La fenêtre vidéo peut être lue dans un environnement de documents. Pour ce faire, la fenêtre doit être un enfant d’une autre fenêtre (afin qu’elle soit découpée et déplacée de manière appropriée). Cette propriété permet de définir et de récupérer le propriétaire de la fenêtre. Quand la fenêtre appartient à une autre fenêtre, elle appelle simplement la fonction Microsoft Win32 **SetParent,** . Une application qui appelle cette fonction modifie les styles de fenêtre pour définir le \_ bit WS Child sur.

Lorsque la fenêtre appartient à une autre fenêtre, elle transfère automatiquement certains ensembles de messages (en particulier, les messages de la souris et du clavier). Cela permet à une application d’effectuer une modification simple à chaud et d’autres interactions.

Cette fonction membre est destinée à être appelée par des objets externes par le biais de l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . elle verrouille donc la section critique à synchroniser avec le filtre associé. Appelez la fonction membre [**CBaseControlWindow :: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) pour récupérer cette propriété si vous n’appelez pas à partir d’un objet externe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




