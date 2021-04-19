---
description: La méthode SpliceWithNext joint l’objet source à un autre objet source.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'IAMTimelineSrc :: SpliceWithNext, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525152"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>IAMTimelineSrc :: SpliceWithNext, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SpliceWithNext` méthode joint l’objet source à un autre objet source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNext* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source à joindre à la source actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs de retour possibles sont les suivantes :



| Code de retour                                                                                   | Description                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération réussie.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argument non valide.<br/>                                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L’objet spécifié par le paramètre *pNext* n’est pas un objet source.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Argument de pointeur **null** .<br/>                                    |



 

## <a name="remarks"></a>Notes

Comme c’est actuellement le cas, cette méthode ignore les effets sur *pNext*.

Pour que cette méthode aboutisse, *pNext* doit être une trame de correspondance de l’objet source actuel, définie comme suit :

-   Il doit partager le même fichier source.
-   L’heure de début du support doit être égale à l’heure d’arrêt du support de la source actuelle.
-   La vitesse de lecture doit être la même. La vitesse de lecture est la durée du support, divisée par la durée de la chronologie.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




