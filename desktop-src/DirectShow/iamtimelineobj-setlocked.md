---
description: La méthode SetLocked définit l’état de modification de l’objet sur verrouillé ou déverrouillé.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'IAMTimelineObj :: SetLocked, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543269"
---
# <a name="iamtimelineobjsetlocked-method"></a>IAMTimelineObj :: SetLocked, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetLocked` méthode définit l’état de modification de l’objet sur verrouillé ou déverrouillé.

Un état verrouillé indique que l’objet ne doit pas être modifié ; un État déverrouillé indique que l’objet peut être modifié. La chronologie n’applique pas le verrou. Le paramètre verrouillé existe uniquement pour la commodité de l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* 
</dt> <dd>

Valeur booléenne qui spécifie l’état de modification de l’objet. Si la **valeur est true**, l’objet est verrouillé et ne doit pas être modifié. Si la **valeur est false**, l’objet est déverrouillé et peut être modifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




