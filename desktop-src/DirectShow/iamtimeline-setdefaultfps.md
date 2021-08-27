---
description: 'La méthode SetDefaultFPS définit la fréquence d’images de sortie par défaut, en images par seconde. Les groupes utilisent cette valeur comme fréquence d’images par défaut. Pour définir la fréquence d’images d’un groupe, appelez la méthode IAMTimelineGroup :: SetOutputFPS sur le groupe.'
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: 'IAMTimeline :: SetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d98b4ea7a69f527f0a79ddbe559d3602afecd06e4728da23ef3627ed7a313a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052809"
---
# <a name="iamtimelinesetdefaultfps-method"></a>IAMTimeline :: SetDefaultFPS, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetDefaultFPS` méthode définit la fréquence d’images de sortie par défaut, en images par seconde. Les groupes utilisent cette valeur comme fréquence d’images par défaut. Pour définir la fréquence d’images d’un groupe, appelez la méthode [**IAMTimelineGroup :: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) sur le groupe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*i/s* 
</dt> <dd>

Fréquence d’images par défaut, en images par seconde.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




