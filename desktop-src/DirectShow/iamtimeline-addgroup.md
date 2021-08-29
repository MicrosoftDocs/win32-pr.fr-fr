---
description: La méthode AddGroup ajoute un groupe à la chronologie.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'IAMTimeline :: AddGroup, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f9557b7937bc0426d0d0c2d8efc24ada968d047460c2d7b3c2f8b1c4c3abccff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330289"
---
# <a name="iamtimelineaddgroup-method"></a>IAMTimeline :: AddGroup, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `AddGroup` méthode ajoute un groupe à la chronologie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGroup* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) du groupe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                   | Description                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le nombre maximal de groupes est dépassé.<br/> |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L’objet n’est pas un groupe.<br/>         |



 

## <a name="remarks"></a>Remarques

Actuellement, les chronologies prennent en charge un maximum de 32 groupes.

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

 

 




