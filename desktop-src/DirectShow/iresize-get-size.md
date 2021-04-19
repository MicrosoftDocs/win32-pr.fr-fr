---
description: La méthode d’extraction de la \_ taille retourne la taille de sortie actuelle et le mode Stretch.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: 'IResize :: get_Size, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541493"
---
# <a name="iresizeget_size-method"></a>IResize :: méthode d’extraction de la \_ taille

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `get_Size` méthode retourne la taille de sortie actuelle et le mode Stretch.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
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

</dd> <dt>

*pFlag* \[ à\]
</dt> <dd>

Reçoit un indicateur spécifiant le mode Stretch. Pour connaître les valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si le type de sortie n’a pas été défini, le filtre doit retourner les valeurs par défaut. Ces valeurs peuvent être choisies arbitrairement au moment du Design.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

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

 

 




