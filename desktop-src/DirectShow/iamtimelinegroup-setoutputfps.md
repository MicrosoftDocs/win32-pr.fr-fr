---
description: La méthode SetOutputFPS définit la fréquence d’images de sortie non compressées pour ce groupe.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'IAMTimelineGroup :: SetOutputFPS, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545608"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>IAMTimelineGroup :: SetOutputFPS, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetOutputFPS` méthode définit la fréquence d’images de sortie non compressées pour ce groupe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*i/s* 
</dt> <dd>

Fréquence d’images de sortie pour ce groupe, en images par seconde. La valeur ne peut pas être égale à zéro et ne peut pas comporter plus de sept chiffres après la virgule.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Le rendu de la sortie de ce groupe s’exécute à la fréquence d’images spécifiée, et toutes les modifications sur le matériel source sont arrondies à la limite d’image la plus proche, comme défini par la fréquence d’images. Pour des performances optimales, utilisez la même fréquence d’images pour tous les groupes, vidéo et audio.

La méthode [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) remplace la fréquence d’images.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




