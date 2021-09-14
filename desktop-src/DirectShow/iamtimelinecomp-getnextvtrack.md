---
description: La méthode GetNextVTrack récupère la piste virtuelle suivante après une piste virtuelle spécifiée.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'IAMTimelineComp :: GetNextVTrack, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857818"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a>IAMTimelineComp :: GetNextVTrack, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetNextVTrack` méthode récupère la piste virtuelle suivante après une piste virtuelle spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Pointeur vers la piste virtuelle précédente, ou **null** pour récupérer la première piste virtuelle dans la composition.

</dd> <dt>

*ppNextVirtualTrack* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle suivante, par ordre de priorité.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK si la méthode récupère une piste virtuelle, ou la \_ valeur false dans le cas contraire.

## <a name="remarks"></a>Notes

Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

 

 




