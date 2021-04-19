---
description: La méthode AddProp ajoute une propriété à la méthode setter de propriété, avec un tableau de paires heure-valeur qui définissent la valeur de la propriété sur une plage de temps.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'IPropertySetter :: AddProp, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542241"
---
# <a name="ipropertysetteraddprop-method"></a>IPropertySetter :: AddProp, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `AddProp` méthode ajoute une propriété à la méthode setter de propriété, avec un tableau de paires heure-valeur qui définissent la valeur de la propriété sur une plage de temps.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param* \[ dans\]
</dt> <dd>

[**Dexterity \_ Structure PARAM**](dexter-param.md) qui spécifie la propriété. Le membre **nvaleurs** de la structure doit être égal à la taille du tableau donné dans le paramètre *paValue* .

</dd> <dt>

*paValue* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures de [**\_ valeur Dexter**](dexter-value.md) qui contiennent des paires heure-valeur. Le tableau doit être dans l’ordre chronologique croissant. Les heures sont relatives à l’heure de début de l’effet ou de la transition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La première structure de [**\_ valeur Dexterity**](dexter-value.md) doit spécifier un temps de référence de zéro et un indicateur d’interpolation (**dwInterp**) de **DEXTERF \_ Jump**, ou la méthode retourne une erreur.

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




