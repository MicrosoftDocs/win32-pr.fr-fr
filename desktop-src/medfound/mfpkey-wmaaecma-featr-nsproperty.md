---
description: Spécifie si le DSP de capture vocale effectue une suppression du bruit.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: MFPKEY_WMAAECMA_FEATR_NS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524531"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>\_Propriété NS de MFPKEY WMAAECMA \_ Feature \_

Spécifie si le DSP de capture vocale effectue une suppression du bruit.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

1

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

La suppression du bruit est un composant DSP (Digital Signal Processing) qui supprime ou réduit le bruit d’arrière-plan stationnaire dans le signal audio. La suppression du bruit est appliquée après le traitement de l’annulation de l’écho acoustique (AEC) et du tableau du microphone.

Cette propriété peut avoir les valeurs suivantes.



| Valeur | Description                |
|-------|----------------------------|
| 0     | Désactivez la suppression du bruit. |
| 1     | Activez la suppression du bruit.  |



 

La valeur par défaut de cette propriété est 1 (activé). Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
