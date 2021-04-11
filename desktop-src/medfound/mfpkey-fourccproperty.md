---
description: Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: MFPKEY_FOURCC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951666"
---
# <a name="mfpkey_fourcc-property"></a>MFPKEY, \_ propriété FourCC

Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCFOURCC g

## <a name="data-type"></a>Type de données

VT \_ I4 (valeur FourCC)

## <a name="remarks"></a>Notes

Vous devez définir cette valeur avant de récupérer les valeurs des propriétés suivantes à l’aide de **IPropertyBag** ou **IPropertyStore**:

-   [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)

Vous devez utiliser [**IWMCodecProps :: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) pour récupérer les valeurs des propriétés dépendantes du FourCC indiquées précédemment. Lorsque vous utilisez **GetCodecProp**, vous n’avez pas besoin de définir **MFPKEY \_ FourCC**.

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

 

 




