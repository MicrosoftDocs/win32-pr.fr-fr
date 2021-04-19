---
description: 'La méthode GetDefaultFPS récupère la fréquence d’images de sortie par défaut, en images par seconde (FPS). Les groupes utilisent cette valeur comme fréquence d’images par défaut. Pour définir la fréquence d’images d’un groupe, appelez la méthode IAMTimelineGroup :: SetOutputFPS sur le groupe.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'IAMTimeline :: GetDefaultFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528495"
---
# <a name="iamtimelinegetdefaultfps-method"></a>IAMTimeline :: GetDefaultFPS, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `GetDefaultFPS` méthode récupère la fréquence d’images de sortie par défaut, en images par seconde (FPS). Les groupes utilisent cette valeur comme fréquence d’images par défaut. Pour définir la fréquence d’images d’un groupe, appelez la méthode [**IAMTimelineGroup :: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) sur le groupe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFPS* 
</dt> <dd>

Reçoit la fréquence d’images par défaut, en images par seconde.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




