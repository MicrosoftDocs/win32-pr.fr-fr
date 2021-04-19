---
description: Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521977"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>MFPKEY \_ propriété BUFFERFULLNESSINFIRSTBYTE

Spécifie si le flux de bits vidéo encodé contient une valeur de saturation de la mémoire tampon avec chaque image clé.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCBufferFullnessInFirstByte g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="remarks"></a>Notes

Vous devez définir un type de sortie avant d’obtenir cette valeur.

Vous pouvez récupérer la valeur de cette propriété à l’aide de [IWMCodecProps :: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Si vous utilisez **IPropertyBag**, vous devez d’abord définir la valeur FourCC du format compressé souhaité avec la [propriété \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .

La saturation de la mémoire tampon dans le premier octet de toutes les images clés vous permet de déterminer la taille de mémoire tampon requise lors de la concaténation de flux vidéo compressés.

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

 

 




