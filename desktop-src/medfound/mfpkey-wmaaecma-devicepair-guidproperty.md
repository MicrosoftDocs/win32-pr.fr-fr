---
description: Identifie la combinaison de périphériques audio actuellement utilisée par l’application avec le DSP de capture vocale.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174bbae3c83ef28ece7d05e36b0a05813078a9a9fba73ac7fae7dba25b67fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973328"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID, propriété

Identifie la combinaison de périphériques audio actuellement utilisée par l’application avec le DSP de capture vocale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

\_CLSID VT

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

Définissez cette propriété si vous utilisez le DSP en mode filtre et que la valeur de la propriété [MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ Statistic](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) est \_ true.

Lorsque la propriété [**MFPKEY \_ WMAAECMA Retrieve des \_ \_ \_ statistiques TS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) est \_ définie sur true, le DSP collecte des statistiques sur les horodatages à partir des périphériques audio et stocke ces informations dans le registre. Ces statistiques peuvent changer pour chaque combinaison de périphérique de capture audio et de périphérique de rendu audio. Par conséquent, l’application doit assigner un GUID pour identifier la combinaison particulière d’appareils en cours d’utilisation. L’application doit effectuer le suivi de ce GUID pour pouvoir attribuer le même GUID chaque fois qu’il utilise la même paire de périphériques audio.

Si vous utilisez le DSP en mode Source, vous n’avez pas besoin de définir cette propriété. Le DSP génère automatiquement un GUID basé sur la valeur de la propriété d’index de l' [ \_ \_ appareil \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-device-indexesproperty.md) .

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

 

 
