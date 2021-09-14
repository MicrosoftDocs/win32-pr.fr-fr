---
description: Spécifie le niveau de puissance pour le décodeur.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313817"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>MFPKEY \_ propriété AVDecVideoSWPowerLevel

Spécifie le niveau de puissance pour le décodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

**100**

## <a name="remarks"></a>Notes

Cette propriété doit être définie sur l’une des valeurs suivantes.



| Valeur | Signification                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Le décodeur utilise un niveau de puissance optimisé pour la durée de vie de la batterie.  |
| 50    | Le décodeur utilise un niveau de puissance équilibré.                            |
| 100   | Le décodeur utilise un niveau de puissance optimisé pour la qualité vidéo. |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
