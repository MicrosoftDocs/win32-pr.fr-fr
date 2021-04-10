---
description: Spécifie si le DSP de capture vocale utilise le mode source ou le mode filtre.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201888"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>\_Propriété du \_ \_ mode source \_ MFPKEY WMAAECMA DMO

Spécifie si le DSP de capture vocale utilise le mode source ou le mode filtre.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ true

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

En mode Source, l’application n’a pas besoin d’envoyer des données d’entrée au DSP, car le DSP extrait automatiquement les données des périphériques audio. En mode filtre, l’application doit envoyer les données d’entrée au DSP.

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description  |
|----------------|--------------|
| VARIANTE \_ false | Mode filtre. |
| VARIANTE \_ true  | Mode Source. |



 

> [!Note]  
> Lorsque DMO est en mode Source, vous devez uniquement appeler [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) pour définir le format de flux de sortie et n’appelez pas [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) pour définir des formats de flux d’entrée. Sinon, l’initialisation DMO échoue.

 

Si la valeur de cette propriété est \_ true, le fournisseur de base de données n’a aucune entrée. Si la valeur est \_ false, le DSP a une ou deux entrées, en fonction de la valeur de la propriété [MFPKEY \_ WMAAECMA \_ System \_ mode](mfpkey-wmaaecma-system-modeproperty.md) , comme indiqué dans le tableau suivant.



| Valeur                     | Nombre d'entrées |
|---------------------------|------------------|
| \_tableau OPTIBEAM \_ et \_ AEC | 2                |
| \_tableau OPTIBEAM \_ uniquement     | 1                |
| \_AEC à canal unique \_      | 2                |
| \_NSAGC à canal unique \_    | 1                |



 

> [!Note]  
> Seuls les modes avec une seule entrée fonctionnent avec le filtre de wrapper DMO à partir de l’API DirectShow 9,0.

 

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

 

 
