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
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234095"
---
# <a name="iamtimelineaddgroup-method"></a>IAMTimeline :: AddGroup, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

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

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                   | Description                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le nombre maximal de groupes est dépassé.<br/> |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L’objet n’est pas un groupe.<br/>         |



 

## <a name="remarks"></a>Notes

Actuellement, les chronologies prennent en charge un maximum de 32 groupes.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




