---
description: Spécifie si la capture de la voix DSP effectue un découpage central.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: MFPKEY_WMAAECMA_FEATR_CENTER_CLIP, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daf1e4b5760642b72f50c645306739592fe866eaeb8c424d08e2717d9835f839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953539"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>MFPKEY \_ WMAAECMA \_ Feature de la \_ \_ propriété Clip

Spécifie si la capture de la voix DSP effectue un découpage central.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ true

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

Le découpage de centre est un processus qui supprime les petits reliquats d’écho restant après le traitement AEC, dans des situations à simple conversion (lorsque la parole se produit uniquement sur une extrémité de la ligne).

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description              |
|----------------|--------------------------|
| VARIANTE \_ false | Désactivez le découpage du centre. |
| VARIANTE \_ true  | Activez le découpage du centre.  |



 

La valeur par défaut de cette propriété est \_ true (activé). Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.

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

 

 
