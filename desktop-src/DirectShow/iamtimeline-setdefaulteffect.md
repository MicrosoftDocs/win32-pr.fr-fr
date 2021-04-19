---
description: La méthode SetDefaultEffect définit l’effet par défaut. Si le moteur de rendu ne peut pas restituer un effet, il remplace l’effet par défaut.
ms.assetid: 6ee94d86-c27f-4378-9a10-f3993a3ae657
title: 'IAMTimeline :: SetDefaultEffect, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 33e23070a7bb10dd040d08c145bfe1e0111026d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544082"
---
# <a name="iamtimelinesetdefaulteffect-method"></a>IAMTimeline :: SetDefaultEffect, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetDefaultEffect` méthode définit l’effet par défaut. Si le moteur de rendu ne peut pas restituer un effet, il remplace l’effet par défaut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGuid* 
</dt> <dd>

Pointeur vers le GUID de l’effet par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si vous ne définissez pas d’effet par défaut ou si l’effet que vous spécifiez comme valeur par défaut provoque une erreur, l’algorithme DES utilise son propre effet par défaut.

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

 

 




