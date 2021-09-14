---
description: La méthode GetCountOfType récupère le nombre d’objets du type spécifié qui sont contenus dans un groupe spécifié et tous ses enfants.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'IAMTimeline :: GetCountOfType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006621"
---
# <a name="iamtimelinegetcountoftype-method"></a>IAMTimeline :: GetCountOfType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetCountOfType` méthode récupère le nombre d’objets du type spécifié qui sont contenus dans un groupe spécifié et tous ses enfants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Groupe* 
</dt> <dd>

Numéro d’index du groupe pour lequel le nombre doit être récupéré.

</dd> <dt>

*pVal* 
</dt> <dd>

Reçoit le nombre d’objets du type spécifié contenus dans le groupe et toutes ses pistes virtuelles, de manière récursive.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Reçoit le nombre renvoyé dans *pval* plus le nombre de compositions recherchées, y compris celui-ci.

</dd> <dt>

*MajorType* 
</dt> <dd>

Membre du type énuméré de la [**chronologie \_ principale \_**](timeline-major-type.md) , en spécifiant le type d’objet à compter.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                  | Description                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Numéro de groupe non valide.<br/>      |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/> |



 

## <a name="remarks"></a>Notes

L’appel de cette méthode équivaut à appeler [**IAMTimelineComp :: GetCountOfType**](iamtimelinecomp-getcountoftype.md) sur le groupe spécifié. Pour plus d’informations, consultez la section Notes de cette méthode.

En règle générale, une application n’appelle pas cette méthode. Elle est appelée en interne par le moteur de rendu.

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

 

 




