---
description: La méthode VTrackSwapPriorities bascule les niveaux de priorité de deux pistes.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'IAMTimelineComp :: VTrackSwapPriorities, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eb67e07f96ec2e8377690a5cd5233ba6cdb40242870da6d5f23b5f404b77b890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999282"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>IAMTimelineComp :: VTrackSwapPriorities, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `VTrackSwapPriorities` méthode change les niveaux de priorité de deux pistes.

Étant donné deux niveaux de priorité, cette méthode bascule les pistes virtuelles à ces priorités. Lorsque la méthode retourne, la piste qui était au premier niveau de priorité est désormais au deuxième niveau de priorité, et vice versa.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

Premier niveau de priorité auquel permuter les pistes virtuelles.

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

Deuxième niveau de priorité auquel permuter les pistes virtuelles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



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

 

 




