---
description: Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.
ms.assetid: 231b7296-ca80-4918-bae6-674b976db24c
title: MFPKEY_WMADRC_PEAKTARGET, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c40fa68e2b580c5d3e8550d6e46c9f6b9fe4bfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517003"
---
# <a name="mfpkey_wmadrc_peaktarget-property"></a>MFPKEY \_ WMADRC \_ PEAKTARGET, propriété

Spécifie le niveau de volume maximal souhaité pour le contenu audio de sortie.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMADRCPeakTarget g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

Consultez la section Notes.

## <a name="remarks"></a>Notes

Vous pouvez définir cette valeur sur le décodeur à des fins de contrôle de plage dynamique, mais il n’aura d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.

Si vous demandez un contrôle de plage dynamique à partir du décodeur lorsque cette propriété n’est pas définie, le codec calcule une valeur par défaut.

Utilisez les propriétés [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) et [MFPKEY \_ WMADRC \_ ](mfpkey-wmadrc-peakrefproperty.md) PEAKREF pour calculer les valeurs appropriées pour cette propriété.

Pour plus d’informations sur le contrôle de plage dynamique, consultez l’article Web [Windows Media Audio fonctionnalités du codec professionnel](/previous-versions/ms867218(v=msdn.10)).

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

 

 
