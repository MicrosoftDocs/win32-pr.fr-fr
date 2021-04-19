---
description: La méthode GetStretchMode récupère le mode Stretch. Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'IAMTimelineSrc :: GetStretchMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f10552ac67c50e8656f303fd524bdad2cd07823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521744"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a>IAMTimelineSrc :: GetStretchMode, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetStretchMode` méthode récupère le mode Stretch. Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pnStretchMode* 
</dt> <dd>

Reçoit un indicateur qui spécifie le mode d’étirement actuel. Pour obtenir la liste des valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




