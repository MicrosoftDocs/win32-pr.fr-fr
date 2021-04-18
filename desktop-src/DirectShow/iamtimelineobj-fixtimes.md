---
description: La méthode FixTimes arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'IAMTimelineObj :: FixTimes, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526484"
---
# <a name="iamtimelineobjfixtimes-method"></a>IAMTimelineObj :: FixTimes, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `FixTimes` méthode arrondit les heures de démarrage et d’arrêt spécifiées aux limites de frame les plus proches, comme défini par le paramètre de fréquence d’images du groupe parent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStart* 
</dt> <dd>

Pointeur vers une variable qui contient l’heure de début, en unités de 100 nanosecondes. Si l’appel a échoué, cette variable est définie sur le temps arrondi.

</dd> <dt>

*pStop* 
</dt> <dd>

Pointeur vers une variable qui contient l’heure d’arrêt, en unités de 100 nanosecondes. Si l’appel a échoué, cette variable est définie sur le temps arrondi.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou E \_ NOTINTREE si l’objet ne fait pas partie d’un groupe.

## <a name="remarks"></a>Notes

Pendant le rendu, DES arrondit les heures de début et de fin de l’objet à la limite d’image la plus proche. Toutefois, les ne remplacent pas les heures de l’objet. Si vous modifiez la fréquence d’images de groupe, les temps arrondis sont toujours calculés à partir des heures d’origine. Pour plus d’informations, consultez [heure dans les services de modification DirectShow](time-in-directshow-editing-services.md).

Utilisez cette méthode pour déterminer les heures de démarrage et d’arrêt précises dans le projet rendu. Par exemple, vous devez rechercher les temps arrondis, plutôt que les heures de début et de fin d’origine de l’objet. Appelez [**IAMTimelineObj :: GetStartStop**](iamtimelineobj-getstartstop.md) pour obtenir les heures d’origine et passer ces valeurs à `FixTimes` .

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
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




