---
description: Spécifie le niveau de puissance pour le décodeur.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce376a370ea6488c87c0266319de7e9bde0a94edab7137a81f015f416ea9fc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874063"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>MFPKEY \_ propriété AVDecVideoSWPowerLevel

Spécifie le niveau de puissance pour le décodeur.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ UI4**

## <a name="default-value"></a>Valeur par défaut

**100**

## <a name="remarks"></a>Remarques

Cette propriété doit être définie sur l’une des valeurs suivantes.



| Valeur | Signification                                                             |
|-------|---------------------------------------------------------------------|
| 0     | Le décodeur utilise un niveau de puissance optimisé pour la durée de vie de la batterie.  |
| 50    | Le décodeur utilise un niveau de puissance équilibré.                            |
| 100   | Le décodeur utilise un niveau de puissance optimisé pour la qualité vidéo. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
