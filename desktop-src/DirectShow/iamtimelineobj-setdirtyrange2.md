---
description: Non implémenté.
ms.assetid: 14ff2979-134f-45e4-98e1-1a119e1ffee2
title: 'IAMTimelineObj :: SetDirtyRange2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7ce2511a4b94f656197cef1bcb2c3cdfb4b4df61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540589"
---
# <a name="iamtimelineobjsetdirtyrange2-method"></a>IAMTimelineObj :: SetDirtyRange2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

Non implémenté.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDirtyRange2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Start* 
</dt> <dd>

Réservé.

</dd> <dt>

*Stop* 
</dt> <dd>

Réservé.

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
</dt> </dl>

 

 




