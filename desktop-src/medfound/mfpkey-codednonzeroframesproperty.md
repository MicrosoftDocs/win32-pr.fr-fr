---
description: Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: MFPKEY_CODEDNONZEROFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1263a15d9ddd678360bf57f5f704143d580d6b17ab63af0777c20d9b09204cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954679"
---
# <a name="mfpkey_codednonzeroframes-property"></a>MFPKEY \_ propriété CODEDNONZEROFRAMES

Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Remarques

Cette valeur est égale à [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) moins les images qui ont été supprimées en raison de contraintes de vitesse de transmission, moins les images de zéro octet. Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples. Des frames de zéro octet peuvent être créés pour des frames en double.

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

 

 
