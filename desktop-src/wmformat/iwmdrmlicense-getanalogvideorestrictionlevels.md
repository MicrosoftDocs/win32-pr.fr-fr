---
title: Méthode IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: La méthode GetAnalogVideoRestrictionLevels récupère toutes les restrictions de la vidéo analogique définies sur la licence actuelle.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Méthode GetAnalogVideoRestrictionLevels format Windows Media
- Méthode GetAnalogVideoRestrictionLevels format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539683"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>IWMDRMLicense :: GetAnalogVideoRestrictionLevels, méthode

La méthode **GetAnalogVideoRestrictionLevels** récupère toutes les restrictions de la vidéo analogique définies sur la licence actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*\[ rgAnalogVideoRestrictions \]* en \[ sortie\]
</dt> <dd>

Reçoit un tableau de structures de [**\_ \_ \_ restrictions de vidéo analogiques WMDRM**](wmdrm-analog-video-restrictions.md) . Affectez la valeur **null** pour récupérer le nombre d’éléments du tableau dans *pcResctrictions*.

</dd> <dt>

*pcRestrictions* \[ in, out\]
</dt> <dd>

Nombre d’éléments dans le tableau de restrictions. Si *rgAnalogVideoRestrictions* a la valeur **null**, cette valeur est définie sur le nombre d’éléments nécessaires dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Vous devez allouer de la mémoire pour le tableau de restrictions. Pour ce faire, appelez d’abord la méthode avec *rgAnalogVideoRestrictions* défini sur **null**, ce qui affectera à *pcRestrictions* la valeur du nombre d’éléments requis.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





