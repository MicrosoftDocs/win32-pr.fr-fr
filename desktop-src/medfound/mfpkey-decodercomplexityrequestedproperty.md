---
description: Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: MFPKEY_DECODERCOMPLEXITYREQUESTED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83330e3e413967d3b97d6531f8bbaf6ebd7809f732885849d0bf7b8f62d55ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954229"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a>MFPKEY \_ propriété DECODERCOMPLEXITYREQUESTED

Spécifie le modèle de conformité de périphérique que vous souhaitez utiliser pour l’encodage vidéo.

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

1

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCDecoderComplexityRequested g

## <a name="data-type-for-ipropertybag"></a>Type de données pour IPropertyBag

VT \_ BSTR

## <a name="default-value-for-ipropertybag"></a>Valeur par défaut pour IPropertyBag

CANAL

## <a name="remarks"></a>Remarques

Le codec tentera d’encoder le contenu à l’aide du modèle de conformité de périphérique spécifié par cette valeur. Le modèle réel auquel le contenu encodé est conforme peut être récupéré à partir de la propriété [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) après l’encodage.

Cette propriété doit avoir l’une des valeurs suivantes.



| Valeur pour IPropertyStore | Valeur pour IPropertyBag | Description         |
|--------------------------|------------------------|---------------------|
| 0                        | SR                   | Profil simple      |
| 1                        | CANAL                   | Profil principal        |
| 2                        | CP                   | n’est plus pris en charge |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




