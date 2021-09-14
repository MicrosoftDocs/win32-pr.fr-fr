---
description: La méthode IsNormalRate indique si le clip sera lu à la vitesse de lecture normale ; autrement dit, la vitesse de lecture du fichier d’origine.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'IAMTimelineSrc :: IsNormalRate, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296699"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>IAMTimelineSrc :: IsNormalRate, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `IsNormalRate` méthode indique si le clip sera lu à la vitesse de lecture normale ; autrement dit, la vitesse de lecture du fichier d’origine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVal* 
</dt> <dd>

Reçoit une valeur booléenne indiquant comment le clip sera rendu. Si la valeur est **true**, le clip est lu au taux normal. Dans le cas contraire, la lecture sera plus rapide ou plus lente que la normale.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Le taux de lecture d’un clip est déterminé par les heures de début et de fin du support, par rapport aux heures de la chronologie :


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Si ce ratio est égal à 1, le clip est lu à la vitesse de création. Dans le cas contraire, la lecture est plus rapide ou plus lente. pour plus d’informations, consultez [l’heure dans DirectShow Services d’édition](time-in-directshow-editing-services.md).

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




