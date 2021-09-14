---
description: Spécifie le nombre de fois que le DSP de capture vocale effectue la suppression de l’écho acoustique (AES) sur le signal résiduel.
ms.assetid: 409b40f8-38eb-49f7-be30-348ab5cdd33a
title: MFPKEY_WMAAECMA_FEATR_AES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5da7505a259a51ca8456f3caffa153790649320
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231732"
---
# <a name="mfpkey_wmaaecma_featr_aes-property"></a>\_Propriété AES de MFPKEY WMAAECMA \_ Fonct \_

Spécifie le nombre de fois que le DSP de capture vocale effectue la suppression de l’écho acoustique (AES) sur le signal résiduel.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Notes

Le DSP de capture vocale peut exécuter AES sur le signal résiduel après l’annulation de l’écho. Cette propriété peut avoir la valeur 0, 1 ou 2. La valeur par défaut est 0. Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

Le DSP utilise cette propriété uniquement lorsque le traitement AEC est activé.

## <a name="requirements"></a>Spécifications



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

 

 
