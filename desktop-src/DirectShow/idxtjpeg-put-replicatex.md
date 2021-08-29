---
description: La \_ méthode put ReplicateX spécifie le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.
ms.assetid: 8baa641c-c063-4c22-8b00-3559c173d627
title: IDxtJpeg ::p ut_ReplicateX, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 64c19df2f827ad7cb0fb0122242ab07c4c88cb58e7e0751fea8fcb62dd649cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982639"
---
# <a name="idxtjpegput_replicatex-method"></a>IDxtJpeg ::p ut \_ ReplicateX, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_ReplicateX` méthode spécifie le nombre de fois que le modèle de réinitialisation est répliqué horizontalement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ReplicateX(
  [in] long newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Nombre de fois où le modèle de réinitialisation est répliqué horizontalement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

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

[**Interface IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




