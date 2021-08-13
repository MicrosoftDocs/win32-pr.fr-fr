---
description: Spécifie si le DSP de capture vocale effectue un contrôle de gain automatique.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f038b18657363677e0953f8fe973c2e3029130ffc2183a08344e1b0cd6905747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343809"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>MFPKEY \_ WMAAECMA \_ Fonct, \_ propriété AGC

Spécifie si le DSP de capture vocale effectue un contrôle de gain automatique.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ false

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

Le contrôle de gain automatique est un composant DSP (Digital Signal Processing) qui ajuste le gain afin que le niveau de sortie du signal reste dans la même plage approximative.

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description                     |
|----------------|---------------------------------|
| VARIANTE \_ false | Désactivez le contrôle de gain automatique. |
| VARIANTE \_ true  | Activez le contrôle du gain automatique.  |



 

La valeur par défaut de cette propriété est \_ false false (désactivé). Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de capture vocale](voicecapturedmo.md)
</dt> </dl>

 

 
