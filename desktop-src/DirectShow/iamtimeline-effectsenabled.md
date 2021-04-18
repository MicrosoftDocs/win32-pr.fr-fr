---
description: La méthode EffectsEnabled détermine si les effets sont activés. Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'IAMTimeline :: EffectsEnabled, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540240"
---
# <a name="iamtimelineeffectsenabled-method"></a>IAMTimeline :: EffectsEnabled, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `EffectsEnabled` méthode détermine si les effets sont activés. Si les effets sont désactivés, ils restent dans la chronologie, mais ne sont pas rendus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Reçoit une valeur booléenne indiquant si les effets sont activés. Si la **valeur est true**, les effets sont activés. Si la **valeur est false**, les effets sont désactivés.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




