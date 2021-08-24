---
description: La méthode GetStartStop récupère les heures de début et de fin de l’objet par rapport au parent de l’objet.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'IAMTimelineObj :: GetStartStop, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400785"
---
# <a name="iamtimelineobjgetstartstop-method"></a>IAMTimelineObj :: GetStartStop, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetStartStop` méthode récupère les heures de début et de fin de l’objet par rapport au parent de l’objet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStart* 
</dt> <dd>

Reçoit l’heure de début, en unités de 100 nanosecondes.

</dd> <dt>

*pStop* 
</dt> <dd>

Reçoit l’heure d’arrêt, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Les compositions, les groupes et les suivis ont toujours une heure de début égale à 0.

Pendant le rendu, DES arrondit les heures de début et de fin d’un objet à la limite d’image la plus proche. Toutefois, les ne remplacent pas les heures de l’objet. Si vous modifiez la fréquence d’images de groupe, les temps arrondis sont toujours calculés à partir des heures d’origine. pour plus d’informations, [reDirectShow les Services d’édition](time-in-directshow-editing-services.md).

Pour déterminer les heures de début et de fin dans le projet rendu, transmettez les valeurs retournées par `GetStartStop` à la méthode [**IAMTimelineObj :: FixTimes**](iamtimelineobj-fixtimes.md) .

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

 

 




