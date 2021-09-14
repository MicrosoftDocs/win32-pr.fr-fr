---
description: La méthode GetRecursiveLayerOfType effectue un classement à profondeur prioritaire des pistes virtuelles contenues dans cette composition, puis récupère la nième piste virtuelle à partir de ce classement.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'IAMTimelineComp :: GetRecursiveLayerOfType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857812"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>IAMTimelineComp :: GetRecursiveLayerOfType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetRecursiveLayerOfType` méthode effectue un classement à profondeur prioritaire des pistes virtuelles contenues dans cette composition, et récupère la *n* ième piste virtuelle à partir de ce classement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppVirtualTrack* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle.

</dd> <dt>

*WhichLayer* 
</dt> <dd>

Spécifie la piste virtuelle à récupérer, indexée à partir de zéro.

</dd> <dt>

*Type* 
</dt> <dd>

Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) qui spécifie s’il faut inclure les suivis dans la recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Aucun objet du type spécifié.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/>       |



 

## <a name="remarks"></a>Notes

En règle générale, une application n’a pas besoin d’appeler cette méthode.

Si le paramètre de *type* est \_ une \_ piste de type principal de chronologie \_ , le classement à profondeur prioritaire comprend des pistes. Si ce n’est pas le cas, il comprend uniquement des compositions et des groupes. L’objet lui-même est inclus dans le classement.

Par exemple, dans l’organisation suivante, à partir de la composition A, le classement serait B, C, F, D, E, A.

![getrecursivelayeroftype](images/composition.png)

Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




