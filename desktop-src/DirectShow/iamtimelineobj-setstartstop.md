---
description: La méthode SetStartStop définit les heures de début et de fin de l’objet par rapport au parent de l’objet.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'IAMTimelineObj :: SetStartStop, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e2806d926c9842f5900f46f923f4cbdf8caa47f112e1832077ab7d2b80a9341c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052449"
---
# <a name="iamtimelineobjsetstartstop-method"></a>IAMTimelineObj :: SetStartStop, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetStartStop` méthode définit les heures de début et de fin de l’objet par rapport au parent de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Start* 
</dt> <dd>

Nouvelle heure de début, en unités de 100 nanosecondes, ou-1 pour conserver l’heure de début existante.

</dd> <dt>

*Stop* 
</dt> <dd>

Nouvelle heure d’arrêt, en unités de 100 nanosecondes, ou-1 pour conserver l’heure d’arrêt existante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide.<br/> |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>    | Non implémenté.<br/>  |



 

## <a name="remarks"></a>Remarques

Les suivis, les compositions et les groupes n’implémentent pas cette méthode. Pour ces objets, l’heure de début est toujours égale à zéro et l’heure d’arrêt est l’heure d’arrêt maximale des objets qu’ils contiennent.

Ne définissez pas les heures qui se chevauchent sur les objets sources au sein d’une même piste. Cela peut entraîner des comportements non définis.

Pour les objets sources, les heures de début et de fin sont indépendantes des heures de début et de fin de support. La modification d’une paire de valeurs ne modifie pas l’autre. Pour définir les heures de début et de fin des médias, appelez la méthode [**IAMTimelineSrc :: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . pour plus d’informations, consultez [l’heure dans DirectShow Services d’édition](time-in-directshow-editing-services.md).

Pour récupérer des transitions et des transitions de trame précises, définissez les paramètres de *démarrage* et d' *arrêt* sur les limites de cadre. Vous pouvez utiliser la méthode [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md) pour convertir une valeur d’heure dans la limite d’image la plus proche, ou utiliser la fonction suivante pour convertir le nombre de frames en temps de référence :


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



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

[**Interface IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




