---
description: La fonction GetDialogSize récupère la taille d’une boîte de dialogue de ressource.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: GetDialogSize, fonction (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533160"
---
# <a name="getdialogsize-function"></a>GetDialogSize fonction)

La fonction **GetDialogSize** récupère la taille d’une boîte de dialogue de ressource.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*iResourceID* 
</dt> <dd>

Identificateur de ressource de la boîte de dialogue.

</dd> <dt>

*pDlgProc* 
</dt> <dd>

Pointeur désignant la procédure de la boîte de dialogue.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur transmise dans le \_ message WM INITDIALOG envoyé à la boîte de dialogue temporaire juste après sa création.

</dd> <dt>

*pResult* 
</dt> <dd>

Pointeur vers une structure de **taille** qui reçoit les dimensions de la boîte de dialogue, en pixels d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la ressource de boîte de dialogue a été trouvée, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Les pages de propriétés peuvent utiliser cette fonction pour retourner la taille d’affichage réelle dont elles ont besoin. La plupart des pages de propriétés sont des boîtes de dialogue et, par conséquent, ont des modèles de boîte de dialogue stockés dans des fichiers de ressources. Les modèles utilisent des unités de boîte de dialogue qui ne correspondent pas directement aux pixels de l’écran. Toutefois, la fonction [**GetPageInfo**](cbasepropertypage-getpageinfo.md) d’une page de propriétés doit retourner la taille réelle de l’affichage en pixels. La page de propriétés peut appeler `GetDialogSize` pour calculer la taille de l’affichage.

Cette fonction crée une instance temporaire de la boîte de dialogue. Pour éviter que la boîte de dialogue ne s’affiche à l’écran, le modèle de boîte de dialogue dans le fichier de ressources ne doit pas avoir de \_ propriété WS visible.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance de page de propriétés](property-page-helper-functions.md)
</dt> </dl>

 

 




