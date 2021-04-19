---
description: Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: MFPKEY_CODEDNONZEROFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529815"
---
# <a name="mfpkey_codednonzeroframes-property"></a>MFPKEY \_ propriété CODEDNONZEROFRAMES

Spécifie le nombre de trames vidéo encodées par le codec qui contiennent réellement des données.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Cette valeur est égale à [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) moins les images qui ont été supprimées en raison de contraintes de vitesse de transmission, moins les images de zéro octet. Vous pouvez récupérer cette valeur une fois que vous avez terminé de passer des exemples. Des frames de zéro octet peuvent être créés pour des frames en double.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
