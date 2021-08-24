---
description: Spécifie le type de détection d’activité vocale effectué par le DSP de capture vocale.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17e23662a8c6966a64140311f24c9af00dc53454cea19c025451698ddbbbd0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953509"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>\_Propriété VAD de MFPKEY WMAAECMA \_ Fonct \_

Spécifie le type de détection d’activité vocale effectué par le DSP de capture vocale.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="applies-to"></a>S'applique à

-   [DSP de capture vocale](voicecapturedmo.md)

## <a name="remarks"></a>Remarques

La valeur de cette propriété est un membre de l’énumération du [ \_ \_ mode de l’AEC AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) . La sortie de la détection d’activité vocale est un nombre compris entre 0 et 3, calculé pour chaque image audio. Le DSP encode le résultat dans le bit le plus bas des deux premiers échantillons audio de chaque trame audio. La signification de la valeur dépend du mode spécifié.

Le code suivant montre comment extraire les résultats des données audio. Dans cet exemple, *pOutput* est un pointeur vers le début d’une image audio dans les données de sortie.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



La valeur par défaut de cette propriété est 0 (désactivé). Avant de définir cette propriété, vous devez affecter à la propriété [ \_ mode de \_ fonctionnalité \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) la \_ valeur variant true.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
