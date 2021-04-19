---
description: La méthode FixMediaTimes arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche, comme défini par la fréquence d’images de sortie. En général, les applications n’ont pas besoin d’appeler cette méthode.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'IAMTimelineSrc :: FixMediaTimes, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532710"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>IAMTimelineSrc :: FixMediaTimes, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `FixMediaTimes` méthode arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche, comme défini par la fréquence d’images de sortie. En général, les applications n’ont pas besoin d’appeler cette méthode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FixMediaTimes(
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

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est similaire à la méthode [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md) , mais elle conserve le rapport d’origine des heures de temps et de chronologie des médias. L’arrondi des heures à la limite de cadre la plus proche risque de déformer ce rapport.

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

 

 




