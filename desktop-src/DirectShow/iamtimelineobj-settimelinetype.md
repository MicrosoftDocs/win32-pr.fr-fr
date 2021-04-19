---
description: 'Non pris en charge. Appelez la méthode IAMTimeline :: CreateEmptyNode pour créer un nouvel objet Timeline. Une fois qu’un objet est créé, vous ne pouvez pas modifier son type.'
ms.assetid: 127b7435-84b0-46c4-b072-bb8eb54b6a4f
title: 'IAMTimelineObj :: SetTimelineType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a63031968a2dfb43d98f9b7f59bd2d9051042732
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541656"
---
# <a name="iamtimelineobjsettimelinetype-method"></a>IAMTimelineObj :: SetTimelineType, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

Non pris en charge. Appelez la méthode [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) pour créer un nouvel objet Timeline. Une fois qu’un objet est créé, vous ne pouvez pas modifier son type.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTimelineType(
   TIMELINE_MAJOR_TYPE newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* 
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

 

 




