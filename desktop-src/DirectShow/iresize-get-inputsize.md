---
description: La \_ méthode d’infiltration retourne la taille d’entrée actuelle du filtre de redimensionnement.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'IResize :: get_InputSize, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b862237f8c51bdf6c22ca9acb667199fadee33b37e425efabfe25bdb8a20dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078929"
---
# <a name="iresizeget_inputsize-method"></a>IResize :: obtient la \_ méthode Input

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `get_InputSize` méthode retourne la taille d’entrée actuelle du filtre de redimensionnement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*piHeight* \[ à\]
</dt> <dd>

Reçoit la hauteur vidéo, en pixels.

</dd> <dt>

*piWidth* \[ à\]
</dt> <dd>

Reçoit la largeur vidéo, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si la broche d’entrée du filtre n’est pas connectée, retourne un code d’erreur. Sinon, retournez la largeur et la hauteur de la vidéo, comme spécifié par le type de média de la broche d’entrée.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 ou version ultérieure<br/>                                                         |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IResize**](iresize.md)
</dt> </dl>

 

 




