---
description: La \_ méthode put owner définit la fenêtre parente de la fenêtre vidéo ; la fenêtre parente transfère ensuite certains messages à la fenêtre vidéo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Méthode CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f33e0c26506faea93afc11f51aaba13007c443fc011839efafce436fe9f2b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635890"
---
# <a name="cbasecontrolwindowput_owner-method"></a>Méthode de propriétaire CBaseControlWindow. put \_

La `put_Owner` méthode définit la fenêtre parente de la fenêtre vidéo ; la fenêtre parente transfère ensuite certains messages à la fenêtre vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Propriétaire* 
</dt> <dd>

Handle vers la fenêtre parente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur.

## <a name="remarks"></a>Remarques

En interne, cette méthode appelle la fonction Microsoft Win32 **SetParent,** pour définir le nouveau propriétaire et définit le style de la fenêtre parente sur WS \_ Child. La fenêtre parente transmet ensuite certains ensembles de messages (en particulier, les messages de souris et de clavier) à la fenêtre vidéo.

Une fois que vous avez défini le propriétaire de la fenêtre vidéo, vous devez définir le propriétaire sur la **valeur null** et le style de fenêtre du propriétaire sur WS \_ OVERLAPPED et WS \_ CLIPCHILDREN avant de libérer le graphique de filtre. Lorsque vous affectez la valeur **null** au propriétaire, cette méthode désactive le bit WS Child de la fenêtre parente \_ . Si vous ne définissez pas le propriétaire sur **null**, la fenêtre parente continue à transmettre des messages à la fenêtre vidéo et des erreurs risquent de se produire au moment de la fermeture de l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




