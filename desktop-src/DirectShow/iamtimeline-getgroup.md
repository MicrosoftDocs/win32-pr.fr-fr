---
description: La méthode GetGroup récupère un groupe spécifié.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'IAMTimeline :: GetGroup, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71bf4aa0dd5d6f338da43d71384ead024fe821d3a639b0021299f6f6deb14be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685189"
---
# <a name="iamtimelinegetgroup-method"></a>IAMTimeline :: GetGroup, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetGroup` méthode récupère un groupe spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppGroup* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) du groupe.

</dd> <dt>

*WhichGroup* 
</dt> <dd>

Index du groupe à récupérer, en fonction de l’ordre dans lequel les groupes ont été ajoutés à la chronologie. Le premier groupe ajouté à la chronologie a un index de 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

 

 




