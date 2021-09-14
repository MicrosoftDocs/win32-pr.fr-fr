---
description: La méthode GetCountOfType récupère le nombre d’objets d’un type donné contenu dans cette composition et toutes ses pistes virtuelles, de manière récursive.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'IAMTimelineComp :: GetCountOfType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857823"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>IAMTimelineComp :: GetCountOfType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetCountOfType` méthode récupère le nombre d’objets d’un type donné contenu dans cette composition et toutes ses pistes virtuelles, de manière récursive.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVal* 
</dt> <dd>

Reçoit le nombre d’objets du type spécifié contenus dans cette composition et toutes ses pistes virtuelles, de manière récursive.

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

Retourne S \_ OK en cas de réussite, ou un pointeur E dans le \_ cas contraire.

## <a name="remarks"></a>Notes

En règle générale, une application n’appelle pas cette méthode. Elle est appelée par le moteur de rendu.

Si vous comptez des compositions, la valeur retournée dans *pval* est égale à zéro et la valeur retournée dans *pValWithComps* est le nombre de compositions. La valeur de *\* pValWithComps* comprend la composition sur laquelle vous appelez la méthode. Par exemple, si vous appelez cette méthode sur une composition vide, *\* pValWithComps* est égal à 1.

Les groupes ne peuvent pas résider dans les compositions. vous ne pouvez donc pas utiliser cette méthode pour compter les groupes. (Le nombre retourné sera toujours égal à zéro.) Pour compter les groupes, appelez la méthode [**IAMTimeline :: GetGroupCount**](iamtimeline-getgroupcount.md) .

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

 

 




