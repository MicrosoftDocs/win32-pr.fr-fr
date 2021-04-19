---
description: La méthode GetEffect récupère l’effet au niveau de priorité spécifié.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'IAMTimelineEffectable :: GetEffect, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523456"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>IAMTimelineEffectable :: GetEffect, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La méthode **GetEffect** récupère l’effet au niveau de priorité spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppFX* \[ à\]
</dt> <dd>

Reçoit l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’effet.

</dd> <dt>

*Et* 
</dt> <dd>

Niveau de priorité de l’effet à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur HRESULT. Il peut prendre les valeurs suivantes :



| Code de retour                                                                               | Description                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Aucun effet à la priorité spécifiée<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Opération réussie.<br/>                             |
| <dl> <dt>**\_pointeur E**</dt> </dl> | Argument de pointeur **null** .<br/>           |



 

## <a name="remarks"></a>Notes

Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




