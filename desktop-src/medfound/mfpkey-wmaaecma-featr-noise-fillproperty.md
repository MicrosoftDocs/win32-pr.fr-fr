---
description: Spécifie si le DSP de capture vocale effectue un remplissage de bruit.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: MFPKEY_WMAAECMA_FEATR_NOISE_FILL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec3f2f6780157da97263bd6e68ac5f38c9448a5633fafe6481b082ed033331dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035117"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>\_Propriété de \_ remplissage du \_ bruit \_ de MFPKEY WMAAECMA

Spécifie si le DSP de capture vocale effectue un remplissage de bruit.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ true

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

Le remplissage du bruit ajoute une petite quantité de bruit aux portions du signal où le découpage de centre a supprimé les échos résiduels. Cela permet à l’utilisateur d’obtenir une meilleure expérience que de laisser des trous silencieux dans le signal.

Cette propriété peut avoir les valeurs suivantes.



| Valeur          | Description            |
|----------------|------------------------|
| VARIANTE \_ true  | Activez le remplissage de bruit.  |
| VARIANTE \_ false | Désactivez le remplissage de bruit. |



 

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

 

 
