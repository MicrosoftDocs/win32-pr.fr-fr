---
description: La méthode CreateEmptyNode crée un nouvel objet Timeline.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: 'IAMTimeline :: CreateEmptyNode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f98073c7e3a4be7fa57858440e540769eef50c44fae4ddcaed459146bfc788a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389139"
---
# <a name="iamtimelinecreateemptynode-method"></a>IAMTimeline :: CreateEmptyNode, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `CreateEmptyNode` méthode crée un nouvel objet Timeline.

Utilisez cette méthode pour créer des objets Timeline, plutôt que la fonction **CoCreateInstance** , car cette méthode exécute des routines d’initialisation importantes. Chaque objet créé par cette méthode prend en charge au moins l’interface [**IAMTimelineObj**](iamtimelineobj.md) , ainsi que d’autres interfaces spécifiques à ce type d’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppObj* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) du nouvel objet.

</dd> <dt>

*Type* 
</dt> <dd>

Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) , en spécifiant le type d’objet à créer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

N’ajoutez pas le nouvel objet à une autre instance de chronologie. Chaque objet d’une chronologie doit être créé par cette chronologie.

Si la méthode est réussie, l’interface [**IAMTimelineObj**](iamtimelineobj.md) qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




