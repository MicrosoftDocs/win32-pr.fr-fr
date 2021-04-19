---
description: La méthode SetStreamNumber spécifie le flux à lire à partir du fichier source associé à cet objet source.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'IAMTimelineSrc :: SetStreamNumber, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541399"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>IAMTimelineSrc :: SetStreamNumber, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetStreamNumber` méthode spécifie le flux à lire à partir du fichier source associé à cet objet source.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Val* 
</dt> <dd>

Numéro de flux, à partir de l’ensemble de flux correspondant au type de média du groupe parent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Le paramètre *Val* spécifie un numéro de flux à partir de l’ensemble de flux qui correspond au type de média du groupe parent, et non à partir de l’ensemble des flux dans le fichier source. Par exemple, supposons qu’un fichier contienne deux flux vidéo et deux flux audio. Si l’objet source est à l’intérieur d’un groupe vidéo, l’affectation de la valeur 0 à *Val* sélectionne le premier flux vidéo. L’appelant est chargé de spécifier un numéro de flux valide.

Le nombre de flux est défini par défaut sur zéro.

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

 

 




