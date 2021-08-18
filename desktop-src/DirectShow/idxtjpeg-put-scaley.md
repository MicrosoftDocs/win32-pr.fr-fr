---
description: La méthode de mise à l' \_ échelle put spécifie le degré d’étirement vertical de la réinitialisation.
ms.assetid: 1dd84540-b249-482c-9cb7-aab8c7dc4d25
title: IDxtJpeg ::p ut_ScaleY, méthode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e16b3e2e94a2878bd425b705544701362242f305471b063cdbaff70cbaba63cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213309"
---
# <a name="idxtjpegput_scaley-method"></a>IDxtJpeg : méthode de mise à l’échelle de :p ut \_

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `put_ScaleY` méthode spécifie la quantité d’étirement vertical de la réinitialisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ScaleY(
  [in] double newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Valeur de l’étirement vertical de la réinitialisation, sous la forme d’un pourcentage de la définition de la réinitialisation d’origine. Par exemple, la valeur 1,0 signifie aucun étirement, et 2,0 signifie l’étirement de 200%.

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

 

 




