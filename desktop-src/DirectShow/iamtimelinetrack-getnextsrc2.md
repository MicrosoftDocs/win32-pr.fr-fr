---
description: 'La méthode GetNextSrc2 recherche dans le suivi la source suivante qui apparaît à l’heure spécifiée ou ultérieurement. Cette méthode est équivalente à IAMTimelineTrack :: GetNextSrc, mais prend une valeur REFTIME.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'IAMTimelineTrack :: GetNextSrc2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543592"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>IAMTimelineTrack :: GetNextSrc2, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetNextSrc2` méthode recherche la source suivante qui apparaît à l’heure spécifiée ou une version ultérieure dans le suivi. Cette méthode est équivalente à [**IAMTimelineTrack :: GetNextSrc**](iamtimelinetrack-getnextsrc.md), mais prend une valeur [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
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

En entrée, contient l’heure de début de la recherche, en secondes. Si la méthode récupère une source, elle définit la valeur sur l’heure d’arrêt de la source. Si la méthode ne récupère pas de source, la valeur devient non valide et l’application ne doit pas l’utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne \_ la valeur OK si la méthode récupère une source, ou la \_ valeur false dans le cas contraire.

## <a name="remarks"></a>Notes

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

 

 




