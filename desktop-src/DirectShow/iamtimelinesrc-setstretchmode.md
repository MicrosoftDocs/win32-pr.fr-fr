---
description: La méthode SetStretchMode définit le mode Stretch. Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'IAMTimelineSrc :: SetStretchMode, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c12d14edf665bb3257b627a194923c267ee9e8bd25027e40a7a975a15c10025f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148542"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>IAMTimelineSrc :: SetStretchMode, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetStretchMode` méthode définit le mode Stretch. Le mode Stretch détermine la façon dont une source vidéo est rendue si sa taille ne correspond pas aux dimensions de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nStretchMode* 
</dt> <dd>

Indicateur qui spécifie le mode d’étirement actuel. Pour obtenir la liste des valeurs possibles, consultez [**indicateurs de redimensionnement**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




