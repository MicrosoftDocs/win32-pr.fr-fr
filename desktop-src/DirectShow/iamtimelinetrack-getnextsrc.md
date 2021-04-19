---
description: La méthode GetNextSrc recherche dans le suivi la source suivante qui apparaît à l’heure spécifiée ou ultérieurement.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'IAMTimelineTrack :: GetNextSrc, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525371"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>IAMTimelineTrack :: GetNextSrc, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetNextSrc` méthode recherche la source suivante qui apparaît à l’heure spécifiée ou une version ultérieure dans le suivi.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppSrc* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.

</dd> <dt>

*pInOut* 
</dt> <dd>

Pointeur vers une variable qui contient l’heure de début de la recherche, en unités de 100 nanosecondes. Si la méthode récupère une source, elle définit la valeur sur l’heure d’arrêt de la source. Si la méthode ne récupère pas de source, la valeur devient non valide et l’application ne doit pas l’utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne \_ la valeur OK si la méthode récupère une source, ou la \_ valeur false dans le cas contraire.

## <a name="remarks"></a>Notes

Si l’heure spécifiée par *pInOut* se situe entre les heures de début et de fin d’une source, la méthode récupère cette source.

Si la méthode retourne la valeur \_ OK, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




